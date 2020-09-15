---
title: Külső felhasználók felvétele terjesztési csoportba
ms.author: chrisda
author: chrisda
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.assetid: caa0f310-0bb7-48e3-8ad2-cb358b53bbba
ms.openlocfilehash: 03cfd2c576cb03cbefd524a4ab6f04e2ef1eebec
ms.sourcegitcommit: c6692ce0fa1358ec3529e59ca0ecdfdea4cdc759
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/14/2020
ms.locfileid: "47663515"
---
# <a name="add-external-users-to-a-distribution-group"></a><span data-ttu-id="75ca5-102">Külső felhasználók felvétele terjesztési csoportba</span><span class="sxs-lookup"><span data-stu-id="75ca5-102">Add external users to a Distribution Group</span></span>

<span data-ttu-id="75ca5-103">Külső partnerek felvétele egy terjesztési csoportba (DG) két lépésből álló folyamat:</span><span class="sxs-lookup"><span data-stu-id="75ca5-103">Adding an external contact to a Distribution Group (DG) is a two-step process:</span></span>
  
1. <span data-ttu-id="75ca5-104">Levelezési névjegykártya létrehozása külső felhasználó számára:</span><span class="sxs-lookup"><span data-stu-id="75ca5-104">Create a Mail Contact for the external user:</span></span>
    
    1. <span data-ttu-id="75ca5-105">A felügyeleti központban lépjen a **felhasználók**  >  [partnerek](https://admin.microsoft.com/adminportal/home#/Contact) lapjára.</span><span class="sxs-lookup"><span data-stu-id="75ca5-105">In the admin center, go to the **Users** > [Contacts](https://admin.microsoft.com/adminportal/home#/Contact) page.</span></span> 
    
    2. <span data-ttu-id="75ca5-106">Jelölje be **a névjegykártya felvétele**jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="75ca5-106">Select **Add a contact**.</span></span>
    
    3. <span data-ttu-id="75ca5-107">Adja meg a névjegy adatait, és válassza a **Hozzáadás**gombot.</span><span class="sxs-lookup"><span data-stu-id="75ca5-107">Type the information for your contact and select **Add**.</span></span>
    
2. <span data-ttu-id="75ca5-108">Adja hozzá a levelezési ügyfelet a DG-hoz:</span><span class="sxs-lookup"><span data-stu-id="75ca5-108">Add the Mail Contact to your DG:</span></span>
    
    1. <span data-ttu-id="75ca5-109">A felügyeleti központban lépjen a **csoportok**  >  [csoportjai](https://admin.microsoft.com/adminportal/home#/groups) lapra.</span><span class="sxs-lookup"><span data-stu-id="75ca5-109">In the admin center, go to the **Groups** > [Groups](https://admin.microsoft.com/adminportal/home#/groups) page.</span></span> 
    
    2. <span data-ttu-id="75ca5-110">Keresse meg azt a Főigazgatóságot, amelyhez hozzá szeretné adni a külső felhasználót, és a Szerkesztés párbeszédpanel megnyitásához jelölje ki azt.</span><span class="sxs-lookup"><span data-stu-id="75ca5-110">Find the DG you want to add the external user to, and select it to open the edit dialog.</span></span>
    
    3. <span data-ttu-id="75ca5-111">A **tagok** lapon válassza az **összes megtekintése és a tagok kezelése**lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="75ca5-111">On the **Members** tab, select **View all and manage members**.</span></span> 
    
    4. <span data-ttu-id="75ca5-112">Válassza a **Tagok hozzáadása**lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="75ca5-112">Select **Add members**.</span></span>
    
    5. <span data-ttu-id="75ca5-113">Jelölje ki az előző lépésben létrehozott levelezési névjegykártyát, és válassza a **Mentés**gombot.</span><span class="sxs-lookup"><span data-stu-id="75ca5-113">Select the Mail Contact you created on the previous step, and then select **Save**.</span></span>
    
<span data-ttu-id="75ca5-114">Ha az alábbi lépéseket követve a külső felhasználók nem tudnak e-maileket küldeni a DG-nek, vagy nem érkeznek meg az e-mailek, akkor lehet, hogy a DG csak a belső felhasználóktól érkező e-mailek engedélyezésére van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="75ca5-114">If after following these steps your external users can't send emails to the DG or don't receive emails from it, it could be that the DG is marked to only allow emails from internal users.</span></span> <span data-ttu-id="75ca5-115">Ezt a konfigurációt követve ellenőrizheti az [itt](https://docs.microsoft.com/exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/fix-error-code-5-7-133-in-exchange-online)leírt útmutatást.</span><span class="sxs-lookup"><span data-stu-id="75ca5-115">You can check this configuration and fix it following the directions [here](https://docs.microsoft.com/exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/fix-error-code-5-7-133-in-exchange-online).</span></span>
  
 <span data-ttu-id="75ca5-116">**Megjegyzés:** Ezek az utasítások nem érvényesek, ha a csoport típusa "Microsoft 365 Group" a "terjesztési csoport" helyett.</span><span class="sxs-lookup"><span data-stu-id="75ca5-116">**Note:** These instructions don't apply if your group's type is "Microsoft 365 group" instead of "Distribution group."</span></span> <span data-ttu-id="75ca5-117">Ebben az esetben a külső felhasználót közvetlenül a csoportba veheti fel az Outlookból.</span><span class="sxs-lookup"><span data-stu-id="75ca5-117">If that is the case, you can add the external user directly to the group from Outlook.</span></span> <span data-ttu-id="75ca5-118">A cikkben részletes információkat talál a Microsoft 365-csoportok vendégeinek, valamint a külső vendégek hozzáadásának lépéseit ismertető [cikkben](https://support.office.com/article/Guest-access-in-Office-365-Groups-bfc7a840-868f-4fd6-a390-f347bf51aff6.aspx).</span><span class="sxs-lookup"><span data-stu-id="75ca5-118">Detailed information on Microsoft 365 Groups guests as well as instructions for adding external guests can be found in [this article](https://support.office.com/article/Guest-access-in-Office-365-Groups-bfc7a840-868f-4fd6-a390-f347bf51aff6.aspx).</span></span>
  