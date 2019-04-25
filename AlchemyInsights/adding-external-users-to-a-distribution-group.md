---
title: Külső felhasználók hozzáadása a terjesztési csoportot?
ms.author: v-crytho
author: CrystalThomasMS
ms.date: 8/22/2017
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.assetid: caa0f310-0bb7-48e3-8ad2-cb358b53bbba
ms.openlocfilehash: ce67797a1838630ab3a42e1eeeefc401a0e3f753
ms.sourcegitcommit: 9d78905c512192ffc4675468abd2efc5f2e4baf4
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32398460"
---
# <a name="adding-external-users-to-a-distribution-group"></a><span data-ttu-id="947f5-102">Külső felhasználók hozzáadása a terjesztési csoportot?</span><span class="sxs-lookup"><span data-stu-id="947f5-102">Adding external users to a Distribution Group?</span></span>

<span data-ttu-id="947f5-103">Hozzáadása egy külső partner, a terjesztési csoport (DG) egy 2 lépésből álló folyamat:</span><span class="sxs-lookup"><span data-stu-id="947f5-103">Adding an external contact to a Distribution Group (DG) is a 2-step process:</span></span>
  
1. <span data-ttu-id="947f5-104">A külső felhasználó levelezési névjegy létrehozása:</span><span class="sxs-lookup"><span data-stu-id="947f5-104">Create a Mail Contact for the external user:</span></span>
    
1. <span data-ttu-id="947f5-105">Kattintson [ide](https://admin.microsoft.com/adminportal/home#/Contact) kattintva keresse meg a kapcsolat lap a portál a.</span><span class="sxs-lookup"><span data-stu-id="947f5-105">Click [here](https://admin.microsoft.com/adminportal/home#/Contact) to navigate to the Contact edit page in the Admin portal.</span></span> 
    
2. <span data-ttu-id="947f5-106">Kattintson a **Partner felvétele**.</span><span class="sxs-lookup"><span data-stu-id="947f5-106">Click on **Add a Contact**.</span></span>
    
3. <span data-ttu-id="947f5-107">Írja be a partner adatait, és kattintson a **Mentés**gombra.</span><span class="sxs-lookup"><span data-stu-id="947f5-107">Type the information for your contact and click **Save**.</span></span>
    
2. <span data-ttu-id="947f5-108">Adja hozzá a levél az ügyfélnek a DG:</span><span class="sxs-lookup"><span data-stu-id="947f5-108">Add the Mail Contact to your DG:</span></span>
    
1. <span data-ttu-id="947f5-109">Kattintson [ide](https://admin.microsoft.com/adminportal/home#/groups) a csoportok lapon keresse meg.</span><span class="sxs-lookup"><span data-stu-id="947f5-109">Click [here](https://admin.microsoft.com/adminportal/home#/groups) to navigate to the Groups page.</span></span> 
    
2. <span data-ttu-id="947f5-110">Keresse meg a külső felhasználó hozzáadása, és a Szerkesztés párbeszédpanel megnyitásához kattintsunk a DG.</span><span class="sxs-lookup"><span data-stu-id="947f5-110">Find the DG you want to add the external user to, and click on it to open the edit dialog.</span></span>
    
3. <span data-ttu-id="947f5-111">Kattintson a **Szerkesztés** gombra a **tagok** listájában.</span><span class="sxs-lookup"><span data-stu-id="947f5-111">Click on the **Edit** button in the **Members** list.</span></span> 
    
4. <span data-ttu-id="947f5-112">**Tagok hozzáadása**parancsára.</span><span class="sxs-lookup"><span data-stu-id="947f5-112">Click on **Add Members**.</span></span>
    
5. <span data-ttu-id="947f5-113">Válassza ki az előző lépésben létrehozott levelezési ügyfelet, és kattintson a **Mentés**gombra.</span><span class="sxs-lookup"><span data-stu-id="947f5-113">Select the Mail Contact you created on the previous step and click **Save**.</span></span>
    
<span data-ttu-id="947f5-114">Ha ezen lépések után is a külső felhasználóknak a DG e-mailek küldése nem, vagy nem kap e-mailek belőle, lehet, hogy a DG e-mailek engedélyezése csak a belső felhasználók számára van megjelölve.</span><span class="sxs-lookup"><span data-stu-id="947f5-114">If even after following these steps your external users can't send emails to the DG or don't receive emails from it, it can be that the DG is marked to only allow emails from internal users.</span></span> <span data-ttu-id="947f5-115">Ellenőrizze a konfigurációt, és javítsa ki a következő utasításokat [Itt](https://support.office.com/article/Fix-email-delivery-issues-for-error-code-5-7-133-in-Office-365-991abc19-7756-438f-abcb-39f69b80f284.aspx)</span><span class="sxs-lookup"><span data-stu-id="947f5-115">You can check this configuration and fix it following the directions [here](https://support.office.com/article/Fix-email-delivery-issues-for-error-code-5-7-133-in-Office-365-991abc19-7756-438f-abcb-39f69b80f284.aspx)</span></span>
  
 <span data-ttu-id="947f5-116">**Megjegyzés:** Ezeket az utasításokat nem alkalmazhatók, ha a csoport típusa "Office 365-csoport" helyett "Terjesztési csoport."</span><span class="sxs-lookup"><span data-stu-id="947f5-116">**Note:** These instructions don't apply if your group's type is "Office 365 group" instead of "Distribution group."</span></span> <span data-ttu-id="947f5-117">Ha ez az eset, hozzáadhatja a külső felhasználó közvetlenül a csoport Outlook vagy az Outlook a weben.</span><span class="sxs-lookup"><span data-stu-id="947f5-117">If that is the case, you can add the external user directly to the group from Outlook or Outlook on the Web.</span></span> <span data-ttu-id="947f5-118">A O365 csoportok vendégek részletes magyarázatát, valamint külső vendégek hozzáadására vonatkozó utasításokat a [cikkben](https://support.office.com/article/Guest-access-in-Office-365-Groups-bfc7a840-868f-4fd6-a390-f347bf51aff6.aspx)található.</span><span class="sxs-lookup"><span data-stu-id="947f5-118">Detailed explanation on O365 groups guests as well as instructions for adding external guests can be found in [this article](https://support.office.com/article/Guest-access-in-Office-365-Groups-bfc7a840-868f-4fd6-a390-f347bf51aff6.aspx).</span></span>
  

