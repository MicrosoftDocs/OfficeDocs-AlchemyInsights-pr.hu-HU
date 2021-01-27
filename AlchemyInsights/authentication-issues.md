---
title: Hitelesítési problémák
ms.author: v-smandalika
author: v-smandalika
manager: dansimp
ms.date: 01/25/2021
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom:
- "7748"
- "9004339"
ms.openlocfilehash: 2f413e863e6aa23548e425de5901f8158e1d48ab
ms.sourcegitcommit: ba3118b7ad5e02756d0e5c2113245090f54370af
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/25/2021
ms.locfileid: "49976851"
---
# <a name="authentication-issues"></a><span data-ttu-id="6f98f-102">Hitelesítési problémák</span><span class="sxs-lookup"><span data-stu-id="6f98f-102">Authentication issues</span></span>

<span data-ttu-id="6f98f-103">**Az Azure Active Directory (Azure AD) biztonsági jogkivonat-szolgáltatásból (STS) visszaküldött AADSTS-hibakódok adatait keresi?**</span><span class="sxs-lookup"><span data-stu-id="6f98f-103">**Looking for information about the AADSTS error codes that are returned from the Azure Active Directory (Azure AD) security token service (STS)?**</span></span> <span data-ttu-id="6f98f-104">További információt az AADSTS hibaleírásokról, javításokról és néhány javasolt kerülő megoldás megkereséséről az [Azure AD hitelesítés és engedélyezés](https://docs.microsoft.com/azure/active-directory/develop/reference-aadsts-error-codes) című cikkben talál.</span><span class="sxs-lookup"><span data-stu-id="6f98f-104">See [Azure AD Authentication and authorization error codes](https://docs.microsoft.com/azure/active-directory/develop/reference-aadsts-error-codes) to find AADSTS error descriptions, fixes, and some suggested workarounds.</span></span>

<span data-ttu-id="6f98f-105">Az engedélyezési hibák több különböző hiba következtében léphetnek fel, amelyek nagy része 401-es vagy 403-as hibát generál.</span><span class="sxs-lookup"><span data-stu-id="6f98f-105">Authorization errors can be a result of several different issues, most of which generate a 401 or 403 error.</span></span> <span data-ttu-id="6f98f-106">Például az alábbi problémák engedélyezési hibákhoz vezethetnek:</span><span class="sxs-lookup"><span data-stu-id="6f98f-106">For example, the following issues can all lead to authorization errors:</span></span>

- <span data-ttu-id="6f98f-107">Helytelen [hozzáférési jogkivonat beszerzési folyamatok](https://docs.microsoft.com/azure/active-directory/develop/authentication-vs-authorization)</span><span class="sxs-lookup"><span data-stu-id="6f98f-107">Incorrect [access token acquisition flows](https://docs.microsoft.com/azure/active-directory/develop/authentication-vs-authorization)</span></span> 
- <span data-ttu-id="6f98f-108">Rosszul konfigurált [engedély hatókörök](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent)</span><span class="sxs-lookup"><span data-stu-id="6f98f-108">Poorly configured [permission scopes](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent)</span></span> 
- <span data-ttu-id="6f98f-109">[Jóváhagyás](https://docs.microsoft.com/azure/active-directory/develop/howto-convert-app-to-be-multi-tenant#understanding-user-and-admin-consent) hiánya</span><span class="sxs-lookup"><span data-stu-id="6f98f-109">Lack of [consent](https://docs.microsoft.com/azure/active-directory/develop/howto-convert-app-to-be-multi-tenant#understanding-user-and-admin-consent)</span></span>

<span data-ttu-id="6f98f-110">A gyakori engedélyezési hibák megoldásához próbálkozzon az alábbi lépésekkel valamelyikével, amely a legjobban megfelel a kapott hibának.</span><span class="sxs-lookup"><span data-stu-id="6f98f-110">To resolve common authorization errors, try the steps provided below which most closely match the error you are receiving.</span></span> <span data-ttu-id="6f98f-111">Több lépés is alkalmazható lehet a kapott hibára.</span><span class="sxs-lookup"><span data-stu-id="6f98f-111">More than one step may apply for an error you are receiving.</span></span>

<span data-ttu-id="6f98f-112">**401 Jogosulatlan hozzáférési hiba: Érvényes a jogkivonata?**</span><span class="sxs-lookup"><span data-stu-id="6f98f-112">**401 Unauthorized error: Is your token valid?**</span></span>

<span data-ttu-id="6f98f-113">Győződjön meg arról, hogy az app a kérés részeként érvényes hozzáférési jogkivonatot ad a Microsoft Graph-hoz.</span><span class="sxs-lookup"><span data-stu-id="6f98f-113">Ensure that your app is presenting a valid access token to Microsoft Graph as part of the request.</span></span> <span data-ttu-id="6f98f-114">Ez a hiba gyakran azt jelzi, hogy a hozzáférési jogkivonat hiányzik a HTTP hitelesítési kérés fejlécében, vagy hogy a jogkivonat érvénytelen vagy lejárt.</span><span class="sxs-lookup"><span data-stu-id="6f98f-114">This error often means that the access token may be missing in the HTTP authenticate request header or that the token is invalid or has expired.</span></span> <span data-ttu-id="6f98f-115">Kifejezetten javasoljuk, hogy a Microsoft Authentication Library (MSAL) használatával szerezze be a hozzáférési jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="6f98f-115">We strongly recommend that you use the Microsoft Authentication Library (MSAL) for access token acquisition.</span></span> <span data-ttu-id="6f98f-116">Ez a hiba akkor is előfordulhat, ha egy személyes Microsoft-fióknak megadott meghatalmazási jogkivonatot próbál használni egy olyan API eléréséhez, amely csak munkahelyi vagy iskolai fiókokat (szervezeti fiókokat) támogat.</span><span class="sxs-lookup"><span data-stu-id="6f98f-116">Additionally, this error may occur if you try to use a delegated access token granted to a personal Microsoft account to access an API that only supports work or school accounts (organizational accounts).</span></span>

<span data-ttu-id="6f98f-117">**403 Tiltott művelet: A megfelelő engedélykészletet választotta ki?**</span><span class="sxs-lookup"><span data-stu-id="6f98f-117">**403 Forbidden error: Have you chosen the right set of permissions?**</span></span>

<span data-ttu-id="6f98f-118">Ellenőrizze, hogy megfelelő engedélykészletet kérte-e az alkalmazás által hívott Microsoft Graph API-k alapján.</span><span class="sxs-lookup"><span data-stu-id="6f98f-118">Ensure that you have requested the correct set of permissions based on the Microsoft Graph APIs your app calls.</span></span> <span data-ttu-id="6f98f-119">Az ajánlott kevésbé kiváltságos engedélyeket a Microsoft Graph API-k összes referenciamódszer-témakörében biztosítjuk.</span><span class="sxs-lookup"><span data-stu-id="6f98f-119">Recommended least-privileged permissions are provided in all the Microsoft Graph API reference method topics.</span></span> <span data-ttu-id="6f98f-120">Ezenkívül ezeket az engedélyeket egy felhasználónak vagy egy rendszergazdának kell megadnia az alkalmazásnak.</span><span class="sxs-lookup"><span data-stu-id="6f98f-120">Additionally, those permissions must be granted to the application by a user or an administrator.</span></span> <span data-ttu-id="6f98f-121">Az engedélyek megadása általában egy jóváhagyási lapon vagy az Azure Portal alkalmazásregisztrációs szolgáltatásának használatával történik.</span><span class="sxs-lookup"><span data-stu-id="6f98f-121">Granting permissions normally happens through a consent page or usage of the Azure Portal application registration blade.</span></span> <span data-ttu-id="6f98f-122">Az alkalmazás **Beállítások** panelén kattintson a **Szükséges engedélyek** elemre, majd kattintson az **Engedélyek megadása** lehetőségre.</span><span class="sxs-lookup"><span data-stu-id="6f98f-122">From the **Settings** blade for the application, click **Required Permissions**, and then click **Grant Permissions**.</span></span> <span data-ttu-id="6f98f-123">További információ:</span><span class="sxs-lookup"><span data-stu-id="6f98f-123">For more information, see:</span></span>

- [<span data-ttu-id="6f98f-124">Microsoft Graph-engedélyek</span><span class="sxs-lookup"><span data-stu-id="6f98f-124">Microsoft Graph permissions</span></span>](https://docs.microsoft.com/graph/permissions-reference) 
- [<span data-ttu-id="6f98f-125">Az Azure AD engedélyeinek és hozzájárulásainak ismertetése</span><span class="sxs-lookup"><span data-stu-id="6f98f-125">Understanding Azure AD permissions and consent</span></span>](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent)

<span data-ttu-id="6f98f-126">**403 Tiltott művelet: Beszerezte az appja a választott engedélyeknek megfelelő jogkivonatot?**</span><span class="sxs-lookup"><span data-stu-id="6f98f-126">**403 Forbidden error: Did your app acquire a token to match chosen permissions?**</span></span>

<span data-ttu-id="6f98f-127">Ellenőrizze, hogy a kért vagy megadott engedélytípusok megegyeznek-e az app által megszerzett hozzáférési jogkivonat-típussal.</span><span class="sxs-lookup"><span data-stu-id="6f98f-127">Ensure that the types of permissions requested or granted match the type of access token that your app acquires.</span></span> <span data-ttu-id="6f98f-128">Előfordulhat, hogy alkalmazásengedélyeket kér és ad ki, de delegált interaktív kódfolyamkódokat használ az ügyfélbeli hitelesítőadat-forgalom jogkivonatai helyett, illetve delegált engedélyeket kér és ad ki, de ügyfél hitelesítőadat-folyam jogkivonatokat használ a delegált kódfolyam jogkivonatok helyett.</span><span class="sxs-lookup"><span data-stu-id="6f98f-128">You might be requesting and granting app permissions but using delegated interactive code flow tokens instead of client credential flow tokens, or requesting and granting delegated permissions but using client credential flow tokens instead of delegated code flow tokens.</span></span>

<span data-ttu-id="6f98f-129">A jogkivonatok beszerzésével kapcsolatos további információért lásd:</span><span class="sxs-lookup"><span data-stu-id="6f98f-129">For more information related to acquiring tokens, see:</span></span>

- [<span data-ttu-id="6f98f-130">Hozzáférés kérése a felhasználók nevében és meghatalmazott engedélyek</span><span class="sxs-lookup"><span data-stu-id="6f98f-130">Get access on behalf of users and delegated permissions</span></span>](https://docs.microsoft.com/graph/auth-v2-user) 
- [<span data-ttu-id="6f98f-131">Azure AD v2.0 – OAuth 2.0 engedélyezési kódfolyam</span><span class="sxs-lookup"><span data-stu-id="6f98f-131">Azure AD v2.0 - OAuth 2.0 authorization code flow</span></span>](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-auth-code-flow) 
- [<span data-ttu-id="6f98f-132">Hozzáférés kérése felhasználó (daemon szolgáltatás) és alkalmazásengedélyek nélkül</span><span class="sxs-lookup"><span data-stu-id="6f98f-132">Get access without a user (daemon service) and application permissions</span></span>](https://docs.microsoft.com/graph/auth-v2-service) 
- [<span data-ttu-id="6f98f-133">Azure AD v2.0 – OAuth 2.0-ügyfél hitelesítőadat-folyam</span><span class="sxs-lookup"><span data-stu-id="6f98f-133">Azure AD v2.0 - OAuth 2.0 client credentials flow</span></span>](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)

<span data-ttu-id="6f98f-134">**403 Tiltott művelet: Jelszó visszaállítása**</span><span class="sxs-lookup"><span data-stu-id="6f98f-134">**403 Forbidden error: Resetting password**</span></span>

<span data-ttu-id="6f98f-135">Jelenleg nincsenek olyan alkalmazásengedélyek, amelyek lehetővé teszik a felhasználói jelszavak visszaállítását.</span><span class="sxs-lookup"><span data-stu-id="6f98f-135">Currently, there are no application permission daemon service-to-service permissions that allow resetting user passwords.</span></span> <span data-ttu-id="6f98f-136">Ezek az API-k csak bejelentkezett rendszergazda interaktív delegált kódfolyamával támogatottak.</span><span class="sxs-lookup"><span data-stu-id="6f98f-136">These APIs are only supported using the interactive delegated code flows with a signed-in administrator.</span></span> <span data-ttu-id="6f98f-137">További információt a [Microsoft Graph engedélyek](https://docs.microsoft.com/graph/permissions-reference) lapján találhat.</span><span class="sxs-lookup"><span data-stu-id="6f98f-137">For more information, see [Microsoft Graph permissions](https://docs.microsoft.com/graph/permissions-reference).</span></span>

<span data-ttu-id="6f98f-138">**403 Tiltott művelet: Van hozzáférése a felhasználónak, és rendelkezik licenccel?**</span><span class="sxs-lookup"><span data-stu-id="6f98f-138">**403 Forbidden: Does the user have access and are they licensed?**</span></span>

<span data-ttu-id="6f98f-139">A delegált kódfolyamatok esetén a Microsoft Graph értékeli, hogy a kérés engedélyezett-e az appnak adott engedélyek és a bejelentkezett felhasználó által biztosított engedélyek alapján.</span><span class="sxs-lookup"><span data-stu-id="6f98f-139">For delegated code flows, Microsoft Graph evaluates whether the request has been allowed based on the permissions granted to the app and the permissions that the signed-in user has.</span></span> <span data-ttu-id="6f98f-140">Ez a hiba általában azt jelzi, hogy a felhasználó nem rendelkezik elegendő jogosultsággal ahhoz, hogy végrehajtsa a kérést, **vagy** hogy a felhasználónak nincs licence a hozzáfért adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="6f98f-140">Generally, this error indicates that the user is not privileged enough to perform the request **or** the user is not licensed for the data being accessed.</span></span> <span data-ttu-id="6f98f-141">Csak a szükséges engedélyekkel vagy licencekkel rendelkező felhasználók tudnak sikeresen kérelmezni.</span><span class="sxs-lookup"><span data-stu-id="6f98f-141">Only users with the required permissions or licenses can make the request successfully.</span></span>

<span data-ttu-id="6f98f-142">**403 Tiltott művelet: Megfelelő forrás API-t választott ki?**</span><span class="sxs-lookup"><span data-stu-id="6f98f-142">**403 Forbidden: Did you select the correct resource API?**</span></span>

<span data-ttu-id="6f98f-143">Az API-szolgáltatások, például a Microsoft Graph, ellenőrzik, hogy az *aud* igény (közönség) a kapott hozzáférési jogkivonatban megegyezik-e a várt értékkel, és ha nem, a 403-as Tiltott művelet hiba történik.</span><span class="sxs-lookup"><span data-stu-id="6f98f-143">API services like Microsoft Graph check that the *aud* claim (audience) in the received access token matches the value it expects for itself, and if not, a 403 Forbidden error occurs.</span></span> <span data-ttu-id="6f98f-144">Gyakori hiba, amely következtében egy Azure AD Graph API-khoz, Outlook API-khoz vagy SharePoint/OneDrive API-khoz beszerzett jogkivonatot hibásan próbál használni a Microsoft Graph hívásához (vagy fordítva).</span><span class="sxs-lookup"><span data-stu-id="6f98f-144">A common mistake resulting in this error is trying to use a token acquired for Azure AD Graph APIs, Outlook APIs, or SharePoint/OneDrive APIs to call Microsoft Graph (or vice versa).</span></span> <span data-ttu-id="6f98f-145">Győződjön meg arról, hogy az adott erőforrás (vagy hatókör) egy olyan jogkivonatot szerez be, amely megfelel az app által hívott API-nak.</span><span class="sxs-lookup"><span data-stu-id="6f98f-145">Ensure that the resource (or scope) your app is acquiring a token for matches the API that the app is calling.</span></span>

<span data-ttu-id="6f98f-146">**400 Hibás kérelem vagy 403 Tiltott művelet: Megfelel a felhasználó a szervezete feltételes hozzáférésre (CA) vonatkozó irányelveinek?**</span><span class="sxs-lookup"><span data-stu-id="6f98f-146">**400 Bad Request or 403 Forbidden: Does the user comply with their organization's conditional access (CA) policies?**</span></span>

<span data-ttu-id="6f98f-147">A szervezet feltételes hozzáférésre vonatkozó házirendje (CA) alapján előfordulhat, hogy egy felhasználó az Ön appján keresztüli hozzáférése a Microsoft Graph-erőforrásokhoz olyan további adatokat igényel, amelyek nem szerepelnek a hozzáférési jogkivonatban, amelyet az app eredetileg megszerzett.</span><span class="sxs-lookup"><span data-stu-id="6f98f-147">Based on an organization's conditional access (CA) policies, a user accessing Microsoft Graph resources via your app may be challenged for additional information that is not present in the access token your app originally acquired.</span></span> <span data-ttu-id="6f98f-148">Ebben az esetben az appban egy **400-as, *interaction_required*** típusú hiba történik a hozzáférési jogkivonat beszerzésekor, vagy egy **403-as, *insufficient_claims*** típusú Microsoft Graph hívása esetén.</span><span class="sxs-lookup"><span data-stu-id="6f98f-148">In this case, your app receives a **400 with an *interaction_required*** error during access token acquisition or a **403 with *insufficient_claims*** error when calling Microsoft Graph.</span></span> <span data-ttu-id="6f98f-149">A hiba megjelenése mindkét esetben további információkat tartalmaz, amelyek bemutatják az engedélyezett végpontnak, hogy a felhasználótól további információkat (például többtényezős hitelesítés vagy eszközregisztrálás) igényeljen.</span><span class="sxs-lookup"><span data-stu-id="6f98f-149">In both cases, the error response contains additional information that can be presented to the authorized endpoint to challenge the user for additional information (like multi-factor authentication or device enrollment).</span></span>

<span data-ttu-id="6f98f-150">A feltételes hozzáféréssel kapcsolatos további információkért lásd:</span><span class="sxs-lookup"><span data-stu-id="6f98f-150">For more information related to conditional access, see:</span></span>

- [<span data-ttu-id="6f98f-151">A feltételes hozzáféréssel kapcsolatos kihívások kezelése az MSAL segítségével</span><span class="sxs-lookup"><span data-stu-id="6f98f-151">Handling conditional access challenges using MSAL</span></span>](https://docs.microsoft.com/azure/active-directory/develop/msal-error-handling-dotnet#conditional-access-and-claims-challenges) 
- [<span data-ttu-id="6f98f-152">Fejlesztői útmutató az Azure Active Directory feltételes hozzáféréséhez</span><span class="sxs-lookup"><span data-stu-id="6f98f-152">Developer guidance for Azure Active Directory conditional access</span></span>](https://docs.microsoft.com/azure/active-directory/develop/v2-conditional-access-dev-guide)

<span data-ttu-id="6f98f-153">\**_Az Azure Active Directory-hitelesítési tár (ADAL) és az Azure AD Graph API (AAD Graph) támogatásának vége_* _</span><span class="sxs-lookup"><span data-stu-id="6f98f-153">\**_End of support for Azure Active Directory Authentication Library (ADAL) and Azure AD Graph API (AAD Graph)_* _</span></span>

- <span data-ttu-id="6f98f-154">2020. június 30-tól kezdődően nem adunk hozzá új funkciókat az Azure Active Directory-hitelesítési tár (ADAL) és az Azure AD Graph API (AAD Graph) szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="6f98f-154">Starting June 30th, 2020, we will no longer add any new features to Azure Active Directory Authentication Library (ADAL) and Azure AD Graph API (AAD Graph).</span></span> <span data-ttu-id="6f98f-155">A jövőben is biztosítani fogunk technikai támogatási és biztonsági frissítéseket, funkciófrissítéseket azonban nem.</span><span class="sxs-lookup"><span data-stu-id="6f98f-155">We will continue to provide technical support and security updates but will no longer provide feature updates.</span></span>
- <span data-ttu-id="6f98f-156">2022. június 30-tól kezdődően véget vetünk az ADAL- és az AAD Graph-támogatásnak, és a továbbiakban nem biztosítunk technikai támogatást és biztonsági frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="6f98f-156">Starting June 30th, 2022, we will end support for ADAL and AAD Graph and will no longer provide technical support or security updates.</span></span>
    - <span data-ttu-id="6f98f-157">Az ADAL-t már meglévő operációs rendszereken használó appok ezután is működnek, de sem technikai támogatásban, sem biztonsági frissítésben nem részesülnek.</span><span class="sxs-lookup"><span data-stu-id="6f98f-157">Apps using ADAL on existing OS versions will continue to work after this time but will not get any technical support or security updates.</span></span>
    - <span data-ttu-id="6f98f-158">Előfordulhat, hogy az AAD Graphot használó appok ezt követően nem kapnak választ az AAD Graph-végponttól.</span><span class="sxs-lookup"><span data-stu-id="6f98f-158">Apps using AAD Graph after this time may no longer receive responses from the AAD Graph endpoint.</span></span>

<span data-ttu-id="6f98f-159">_ *ADAL Migration*\*</span><span class="sxs-lookup"><span data-stu-id="6f98f-159">_ *ADAL Migration*\*</span></span>

<span data-ttu-id="6f98f-160">Javasoljuk, hogy frissítsen a [Microsoft Authentication Library (MSAL)](https://docs.microsoft.com/azure/active-directory/develop/v2-overview) szolgáltatásra, amely a legújabb funkciókat és biztonsági frissítéseket használja.</span><span class="sxs-lookup"><span data-stu-id="6f98f-160">We recommend updating to the [Microsoft Authentication Library (MSAL)](https://docs.microsoft.com/azure/active-directory/develop/v2-overview), which has the latest features and security updates.</span></span> <span data-ttu-id="6f98f-161">Ezt azzal kapcsolatban javasoljuk, hogy a Microsoft az alkalmazásait MSAL-re telepíti át a támogatás megszűnésének határidejére.</span><span class="sxs-lookup"><span data-stu-id="6f98f-161">This recommendation is in the context of Microsoft migrating its applications to MSAL by the end-of-support deadline.</span></span> <span data-ttu-id="6f98f-162">A Microsoft-appok MSAL-be való áttelepítésének célja annak biztosítása, hogy az appok kihasználják az MSAL folyamatos biztonsági és funkciófejlesztéseit.</span><span class="sxs-lookup"><span data-stu-id="6f98f-162">The objective of Microsoft apps' migration to MSAL is to ensure that the apps benefit from MSAL's ongoing security and feature improvements.</span></span>

- [<span data-ttu-id="6f98f-163">Az ADAL GYIK elolvasása</span><span class="sxs-lookup"><span data-stu-id="6f98f-163">Read the ADAL FAQ</span></span>](https://docs.microsoft.com/azure/active-directory/develop/msal-migration#frequently-asked-questions-faq) 
- [<span data-ttu-id="6f98f-164">További információ az appok áttelepítéséről platformonként</span><span class="sxs-lookup"><span data-stu-id="6f98f-164">Learn about how to migrate apps on a per-platform basis</span></span>](https://docs.microsoft.com/azure/active-directory/develop/msal-migration#frequently-asked-questions-faq) 
- <span data-ttu-id="6f98f-165">Ha segítségre van szüksége annak megértéséhez, hogy mely alkalmazásai használják az ADAL-t, javasoljuk, hogy tekintse át valamennyi app forráskódját, és ha lehetséges, független szoftvergyártóktól (ISV-k) vagy alkalmazásszolgáltatóktól is segítséget kérhet.</span><span class="sxs-lookup"><span data-stu-id="6f98f-165">If you need help understanding which of your apps use ADAL, we recommend you review all of your apps' source code, and if applicable, reach out to any independent software vendors (ISVs) or app providers.</span></span> <span data-ttu-id="6f98f-166">A Microsoft terméktámogatási szolgálata a bérlői fiókban a nem Microsoft rendszerű ADAL-appok listáját is biztosítja.</span><span class="sxs-lookup"><span data-stu-id="6f98f-166">Microsoft support can also provide you with a list of all non-Microsoft ADAL apps in your tenant.</span></span>

<span data-ttu-id="6f98f-167">**AAD Graph-áttelepítés**</span><span class="sxs-lookup"><span data-stu-id="6f98f-167">**AAD Graph Migration**</span></span>

<span data-ttu-id="6f98f-168">Az AAD Graphot használó alkalmazások esetén kövesse az [Azure AD Graph-appok áttelepítése a Microsoft Graphba](https://docs.microsoft.com/graph/migrate-azure-ad-graph-planning-checklist?view=graph-rest-1.0&preserve-view=true) témakörben leírtakat.</span><span class="sxs-lookup"><span data-stu-id="6f98f-168">For applications that are using AAD Graph, follow our guidance to [migrate Azure AD Graph apps to Microsoft Graph](https://docs.microsoft.com/graph/migrate-azure-ad-graph-planning-checklist?view=graph-rest-1.0&preserve-view=true).</span></span>

- <span data-ttu-id="6f98f-169">[Az áttelepítési ellenőrzőlista segít az első lépésekben](https://docs.microsoft.com/graph/migrate-azure-ad-graph-planning-checklist).</span><span class="sxs-lookup"><span data-stu-id="6f98f-169">[Our migration checklist provides a getting started point](https://docs.microsoft.com/graph/migrate-azure-ad-graph-planning-checklist).</span></span> 
- <span data-ttu-id="6f98f-170">Az Azure-appok regisztrációs portálján látható, hogy mely alkalmazások használják az AAD Graphot.</span><span class="sxs-lookup"><span data-stu-id="6f98f-170">Your Azure app registration portal shows which applications are using AAD Graph.</span></span> <span data-ttu-id="6f98f-171">Javasoljuk, hogy tekintse át az összes app forráskódját, és ha lehetséges, forduljon bármely szoftverszolgáltatóhoz vagy alkalmazásszolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="6f98f-171">We recommend you review all of your apps' source code, and if applicable, reach out to any ISVs or app providers.</span></span> <span data-ttu-id="6f98f-172">A Microsoft terméktámogatási szolgálata a bérlői fiókban található összes AAD Graph-használatra vonatkozó adatokat is biztosítja.</span><span class="sxs-lookup"><span data-stu-id="6f98f-172">Microsoft support can also provide you the information of all AAD Graph usage in your tenant.</span></span>

 









