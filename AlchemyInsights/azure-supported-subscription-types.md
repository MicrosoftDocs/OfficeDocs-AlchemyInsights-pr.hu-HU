---
title: Támogatott előfizetési típusok
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom:
- "9003560"
- "6675"
ms.openlocfilehash: 46bc60435c3f8477e9f274d90c39d0f1c6a523c6
ms.sourcegitcommit: f8b41ecda6db0b8f64fe0c51f1e8e6619f504d61
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "48807564"
---
# <a name="supported-subscription-types"></a><span data-ttu-id="6cad5-102">Támogatott előfizetési típusok</span><span class="sxs-lookup"><span data-stu-id="6cad5-102">Supported subscription types</span></span>

<span data-ttu-id="6cad5-103">Kérjük, tekintse át a támogatott előfizetési típusokat a további folytatáshoz.</span><span class="sxs-lookup"><span data-stu-id="6cad5-103">Please review the supported subscription types to proceed further.</span></span>

[<span data-ttu-id="6cad5-104">Támogatott előfizetési típusok</span><span class="sxs-lookup"><span data-stu-id="6cad5-104">Supported subscription types</span></span>](https://docs.microsoft.com/azure/billing/billing-subscription-transfer?WT.mc_id=Portal-Microsoft_Azure_Support#supported-subscription-types)

<span data-ttu-id="6cad5-105">**Számlázási tulajdonjog átruházása**</span><span class="sxs-lookup"><span data-stu-id="6cad5-105">**Transfer billing ownership**</span></span>

<span data-ttu-id="6cad5-106">Azure Portal – az átvinni kívánt előfizetést tartalmazó számlázási fiók [rendszergazdája](https://ms.portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="6cad5-106">Azure portal as the [Account Admin](https://ms.portal.azure.com/) of the billing account that has the subscription you want to transfer</span></span>

- <span data-ttu-id="6cad5-107">Keressen a **Cost Management + számlázás** lapon.</span><span class="sxs-lookup"><span data-stu-id="6cad5-107">Search on **Cost Management + Billing** .</span></span> <span data-ttu-id="6cad5-108">Válassza a bal oldali ablaktábla **előfizetések** elemét.</span><span class="sxs-lookup"><span data-stu-id="6cad5-108">Select **Subscriptions** from left-pane.</span></span> <span data-ttu-id="6cad5-109">A hozzáféréstől függően előfordulhat, hogy ki kell választania egy számlázási hatókört, majd **előfizetéseket** vagy **Azure-előfizetéseket** .</span><span class="sxs-lookup"><span data-stu-id="6cad5-109">Depending on the access, you may need to select a billing scope and then **Subscriptions** or **Azure subscriptions** .</span></span>
- <span data-ttu-id="6cad5-110">Válassza a számlázási tulajdonjog átruházása lehetőséget az átvinni kívánt előfizetés esetén</span><span class="sxs-lookup"><span data-stu-id="6cad5-110">Select Transfer billing ownership for the subscription you want to transfer</span></span>
- <span data-ttu-id="6cad5-111">Adja meg egy olyan felhasználó e-mail-címét, aki számlázási rendszergazdája az előfizetés új tulajdonosa lesz, majd válassza az **átadás-összehívás küldése** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="6cad5-111">Enter the email address of a user who's a billing administrator of the account that will be the new owner for the subscription and then select **send transfer request**</span></span>
- <span data-ttu-id="6cad5-112">A felhasználó megkapja az átadási kérést ismertető e-mailt.</span><span class="sxs-lookup"><span data-stu-id="6cad5-112">The user gets an email with instructions to review your transfer request.</span></span> <span data-ttu-id="6cad5-113">Az átadás-összehívás jóváhagyásához a felhasználó kiválasztja a hivatkozást az e-mailben, és követi az útmutatást.</span><span class="sxs-lookup"><span data-stu-id="6cad5-113">To approve the transfer request, the user selects the link in the email and follows the instructions.</span></span>

<span data-ttu-id="6cad5-114">Megjegyzés: Ha az előfizetése számlázási tulajdonjogát egy másik Azure AD-bérlői fiókba ruházza át, az előfizetésben szereplő erőforrások kezeléséhez az összes [szerepkör-alapú hozzáférés-vezérlési (RBAC-)](https://docs.microsoft.com/azure/role-based-access-control/overview?WT.mc_id=Portal-Microsoft_Azure_Support) hozzárendelést véglegesen eltávolítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6cad5-114">Note: If you transfer billing ownership of your subscription to a user's account in another Azure AD tenant, all [role-based access control (RBAC)](https://docs.microsoft.com/azure/role-based-access-control/overview?WT.mc_id=Portal-Microsoft_Azure_Support) assignments to manage resources in the subscription are permanently removed.</span></span> <span data-ttu-id="6cad5-115">Az előfizetésben csak az új tulajdonos férhet hozzá az erőforrások kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="6cad5-115">Only the new owner will have access to manage resources in the subscription.</span></span> <span data-ttu-id="6cad5-116">További információ: [előfizetés átvitele egy másik Azure ad-bérlői fiókba](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/known-issues?WT.mc_id=Portal-Microsoft_Azure_Support).</span><span class="sxs-lookup"><span data-stu-id="6cad5-116">For more information, see [Transferring subscription to a user in another Azure AD tenant](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/known-issues?WT.mc_id=Portal-Microsoft_Azure_Support).</span></span>

<span data-ttu-id="6cad5-117">**Az előfizetés tulajdonjogának átruházása**</span><span class="sxs-lookup"><span data-stu-id="6cad5-117">**Transfer Ownership of Subscription**</span></span>

<span data-ttu-id="6cad5-118">Az előfizetés tulajdonosi átvitelének előfeltételei a role-based Access (RBAC) az előfizetésben lévő erőforrások kezeléséhez elvesztik a hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="6cad5-118">Subscription Ownership Transfer prerequisites role based access (RBAC) to manage resources in the subscription lose their access.</span></span> <span data-ttu-id="6cad5-119">Ha szeretne többet megtudni arról, hogy miként vehet fel meglévő előfizetést bérlői fiókba, olvassa el [Az Azure-előfizetés társítása vagy hozzáadása az Azure Active Directoryhoz](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-how-subscriptions-associated-directory?WT.mc_id=Portal-Microsoft_Azure_Support)című témakört</span><span class="sxs-lookup"><span data-stu-id="6cad5-119">For more information about adding an existing subscription to a tenant, see [Associate or add an Azure subscription to Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-how-subscriptions-associated-directory?WT.mc_id=Portal-Microsoft_Azure_Support).</span></span>

- <span data-ttu-id="6cad5-120">A meglévő számlázási ciklusból származó meglévő hátralékos előfizetés átvitele az új fiókba nem kerül át az új fizetési instrumentumba.</span><span class="sxs-lookup"><span data-stu-id="6cad5-120">Subscription Transfer with an existing outstanding amount from the current billing cycle will not be transferred to the new payment instrument in the new account.</span></span> <span data-ttu-id="6cad5-121">Az új fiókba tartozó felhasználók számára elérhető egyetlen adat az előfizetés utolsó havi költsége.</span><span class="sxs-lookup"><span data-stu-id="6cad5-121">The only information available to the users in new account is the last month's cost for your subscription.</span></span> <span data-ttu-id="6cad5-122">A többi használat és a számlázási előzmények nem adják át az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6cad5-122">The rest of the usage and billing history does not transfer with the subscription.</span></span>
- <span data-ttu-id="6cad5-123">A vállalati szerződési (EA) előfizetések számlázási tulajdonjogának átvitele jelenleg a nagyvállalati szerződés portálon érhető el.</span><span class="sxs-lookup"><span data-stu-id="6cad5-123">Transfer billing ownership of Enterprise Agreement (EA) subscriptions is currently supported in the Enterprise Agreement Portal only</span></span>
- <span data-ttu-id="6cad5-124">A kredit-orientált előfizetések, például a Visual Studio, a BizSpark, a Microsoft partner hálózat új felhasználóknak való átviteléhez Visual Studio/Microsoft partner hálózati licenccel kell rendelkeznie az átadás-összehívás elfogadásához.</span><span class="sxs-lookup"><span data-stu-id="6cad5-124">Transferring a credit-oriented subscription like Visual Studio, BizSpark, Microsoft Partner Network to a new user requires to have a Visual Studio/Microsoft partner network license to accept the transfer request</span></span>
- <span data-ttu-id="6cad5-125">Minden erőforrás, például a virtuális gépek, a lemezek és a webhelyek sikeres átadása az új fiókba.</span><span class="sxs-lookup"><span data-stu-id="6cad5-125">All resources like Virtual Machines, disks, and websites transfer to the new account successfully.</span></span> <span data-ttu-id="6cad5-126">A következő erőforrásokat érintheti a több bérlői előfizetés átvitele:</span><span class="sxs-lookup"><span data-stu-id="6cad5-126">The following resources could be affected in a cross-tenant subscription transfer:</span></span>

<span data-ttu-id="6cad5-127">**Azure AD Domain Services**</span><span class="sxs-lookup"><span data-stu-id="6cad5-127">**Azure AD Domain Services**</span></span>

<span data-ttu-id="6cad5-128">Azure fő pince-tárolók</span><span class="sxs-lookup"><span data-stu-id="6cad5-128">Azure Key Vaults</span></span>

- <span data-ttu-id="6cad5-129">Az SQL-alapú [kapcsolódó felhasználók és adatbázisok](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?WT.mc_id=Portal-Microsoft_Azure_Support) hatással lehetnek, különösen akkor, ha az ügyfél Azure Active Directory-alapú hitelesítést használ</span><span class="sxs-lookup"><span data-stu-id="6cad5-129">[SQL related users and databases](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?WT.mc_id=Portal-Microsoft_Azure_Support) could be impacted, especially if the customer uses an Azure Active Directory related authentication</span></span>
- <span data-ttu-id="6cad5-130">Az Azure Active Directory-hitelesítéssel konfigurált **app-szolgáltatások** hatással lehetnek</span><span class="sxs-lookup"><span data-stu-id="6cad5-130">**App Services** configured with Azure Active Directory authentication could be impacted</span></span>
- <span data-ttu-id="6cad5-131">**Visual Studio-csapat** Az Azure-előfizetésekhez kapcsolódó szolgáltatások átmenetileg elveszíthetik az Accessben, amikor a csatlakoztatott Azure-előfizetés meg van szakítva</span><span class="sxs-lookup"><span data-stu-id="6cad5-131">**Visual Studio Team** Services accounts connected to Azure subscriptions may temporarily lose access when the connected Azure subscription is cancelled</span></span>

<span data-ttu-id="6cad5-132">**Ajánlott dokumentumok**</span><span class="sxs-lookup"><span data-stu-id="6cad5-132">**Recommended Documents**</span></span>

<span data-ttu-id="6cad5-133">A számlázási tulajdonjog elfogadása után elvégzendő lépések:</span><span class="sxs-lookup"><span data-stu-id="6cad5-133">Steps after accepting billing ownership:</span></span>

- <span data-ttu-id="6cad5-134">Ha meg szeretné őrizni a számlázási tulajdonjogot, de módosítani szeretné az előfizetését, olvassa el a következő témakört: [Az Azure-előfizetés váltása másik ajánlatra](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer?WT.mc_id=Portal-Microsoft_Azure_Support)</span><span class="sxs-lookup"><span data-stu-id="6cad5-134">To retain billing ownership, but change the type of your subscription, refer: [Switch your Azure subscription to another offer](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer?WT.mc_id=Portal-Microsoft_Azure_Support)</span></span>
- [<span data-ttu-id="6cad5-135">A Visual Studio, a Microsoft Partner Network (MPN) és a kifizetések átvitele a dev/próba-előfizetések segítségével</span><span class="sxs-lookup"><span data-stu-id="6cad5-135">Transferring Visual Studio, Microsoft Partner Network (MPN) and Pay as you go Dev/Test subscriptions</span></span>](https://docs.microsoft.com/azure/billing/billing-subscription-transfer?WT.mc_id=Portal-Microsoft_Azure_Support#transferring-visual-studio-microsoft-partner-network-mpn-and-pay-as-you-go-devtest-subscriptions)
- [<span data-ttu-id="6cad5-136">A vállalati szerződés (EA) előfizetések számlázási tulajdonjogának átvitele</span><span class="sxs-lookup"><span data-stu-id="6cad5-136">Transfer billing ownership of Enterprise Agreement (EA) subscriptions</span></span>](https://docs.microsoft.com/azure/billing/billing-subscription-transfer?WT.mc_id=Portal-Microsoft_Azure_Support#transfer-billing-ownership-of-enterprise-agreement-ea-subscriptions)
- [<span data-ttu-id="6cad5-137">Tulajdonosi kérdések átvitele</span><span class="sxs-lookup"><span data-stu-id="6cad5-137">Transfer Ownership FAQ</span></span>](https://docs.microsoft.com/azure/billing/billing-subscription-transfer?WT.mc_id=Portal-Microsoft_Azure_Support#frequently-asked-questions-faq-for-senders)
- [<span data-ttu-id="6cad5-138">Átvitel tulajdonjogával kapcsolatos problémák elhárítása</span><span class="sxs-lookup"><span data-stu-id="6cad5-138">Troubleshoot Transfer ownership issues</span></span>](https://docs.microsoft.com/azure/billing/billing-subscription-transfer?WT.mc_id=Portal-Microsoft_Azure_Support#troubleshooting)