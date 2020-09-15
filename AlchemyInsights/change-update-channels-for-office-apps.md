---
title: Az Office-alkalmazások frissítési csatornáinak módosítása
ms.author: pebaum
author: pebaum
manager: scotv
ms.date: 07/27/2020
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom:
- "1740"
- "9000140"
ms.openlocfilehash: 4939682a6ca95c4f5475ee6aedea48c9ce83df7f
ms.sourcegitcommit: b10cea11b4975354b91193327b58aa4740d34833
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/28/2020
ms.locfileid: "45439389"
---
# <a name="change-update-channels-for-office-apps"></a><span data-ttu-id="e8ff4-102">Az Office-alkalmazások frissítési csatornáinak módosítása</span><span class="sxs-lookup"><span data-stu-id="e8ff4-102">Change update channels for Office apps</span></span>

<span data-ttu-id="e8ff4-103">Új Office-telepítések esetén az Office szoftverletöltési beállításai val jelölheti ki a kívánt frissítési csatornát, majd telepítse (vagy telepítse újra) az Office-alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-103">For new Office installations, use Office Software Download Settings to select the desired update channel, and then install (or re-install) Office apps.</span></span> <span data-ttu-id="e8ff4-104">További információt a [Szoftverletöltési beállítások kezelése az Office 365-ben ( Szoftverletöltési beállítások kezelése ) témakörben talál.](https://docs.microsoft.com/deployoffice/manage-software-download-settings-office-365)</span><span class="sxs-lookup"><span data-stu-id="e8ff4-104">For more info, see [Manage software download settings in Office 365](https://docs.microsoft.com/deployoffice/manage-software-download-settings-office-365).</span></span> 

<span data-ttu-id="e8ff4-105">**Megjegyzés:** Az Office szoftverletöltési beállításai val kiválasztott frissítési csatorna minden olyan felhasználóra vonatkozik, aki új telepítést hajt végre az O365 portálon.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-105">**Note** The update channel selected using the Office Software Download Settings applies to all users performing new installations using the O365 portal.</span></span> <span data-ttu-id="e8ff4-106">További információt a [Microsoft 365 vagy az Office 2019 letöltése vagy újratelepítése PC-re vagy Mac gépre című témakörben talál.](https://support.microsoft.com/office/download-and-install-or-reinstall-microsoft-365-or-office-2019-on-a-pc-or-mac-4414eaaf-0478-48be-9c42-23adc4716658)</span><span class="sxs-lookup"><span data-stu-id="e8ff4-106">For more info, see [Download and install or reinstall Microsoft 365 or Office 2019 on a PC or Mac](https://support.microsoft.com/office/download-and-install-or-reinstall-microsoft-365-or-office-2019-on-a-pc-or-mac-4414eaaf-0478-48be-9c42-23adc4716658).</span></span>   

<span data-ttu-id="e8ff4-107">Meglévő Office-telepítések esetén az Office-telepítő eszközzel (ODT) másik frissítési csatornára válthat:</span><span class="sxs-lookup"><span data-stu-id="e8ff4-107">For existing Office installations, use the Office Deployment Tool (ODT) to switch to a different update channel:</span></span>  

1. <span data-ttu-id="e8ff4-108">Töltse le az Office telepítőeszköz (setup.exe) legújabb verzióját a [Microsoft letöltőközpontjából.](https://go.microsoft.com/fwlink/p/?LinkID=626065)</span><span class="sxs-lookup"><span data-stu-id="e8ff4-108">Download the latest version of the Office Deployment Tool (setup.exe) from the [Microsoft Download Center](https://go.microsoft.com/fwlink/p/?LinkID=626065).</span></span>
2. <span data-ttu-id="e8ff4-109">Azonosítsa annak a csatornának a nevét, amelyre váltani szeretne.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-109">Identify the name of the channel that you want to switch to.</span></span> <span data-ttu-id="e8ff4-110">További információt [az Office-telepítőeszköz konfigurációs beállításai című témakörben talál.](https://docs.microsoft.com/DeployOffice/configuration-options-for-the-office-2016-deployment-tool#channel-attribute-part-of-add-element)</span><span class="sxs-lookup"><span data-stu-id="e8ff4-110">For more info, see [Configuration options for the Office Deployment Tool](https://docs.microsoft.com/DeployOffice/configuration-options-for-the-office-2016-deployment-tool#channel-attribute-part-of-add-element).</span></span>
3. <span data-ttu-id="e8ff4-111">Hozzon létre egy konfigurációs XML-fájlt, amely megadja a megfelelő csatornanevet, például update.xml.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-111">Create a configuration XML file specifying the appropriate channel name, for example, update.xml.</span></span>  
    <span data-ttu-id="e8ff4-112">a.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-112">a.</span></span> <Configuration>  
    <span data-ttu-id="e8ff4-113">b.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-113">b.</span></span> <span data-ttu-id="e8ff4-114"><Frissítések **Channel ="Havi"** /></span><span class="sxs-lookup"><span data-stu-id="e8ff4-114"><Updates **Channel="Monthly"** /></span></span>  
    <span data-ttu-id="e8ff4-115">c.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-115">c.</span></span> </Configuration>
4. <span data-ttu-id="e8ff4-116">Rendszergazda jogú parancssorból váltson arra a mappára, ahol setup.exe található, és futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="e8ff4-116">From an elevated command prompt, switch to the folder location where setup.exe resides and run the following command:</span></span>  
    <span data-ttu-id="e8ff4-117">a.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-117">a.</span></span> <span data-ttu-id="e8ff4-118">setup.exe /configure update.xml</span><span class="sxs-lookup"><span data-stu-id="e8ff4-118">setup.exe /configure update.xml</span></span>
5. <span data-ttu-id="e8ff4-119">Indítson el egy Office-alkalmazást (például az Excelt), majd válassza a **File**  >  **Fájlfiók**lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-119">Start an Office application (such as Excel), and then select **File** > **Account**.</span></span> <span data-ttu-id="e8ff4-120">A Termékinformáció csoportban válassza a **Frissítési beállítások**  >  **frissítése most**lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-120">In the Product Information section, select **Update Options** > **Update Now**.</span></span>

<span data-ttu-id="e8ff4-121">További információt a [Meglévő Office-alkalmazások frissítési csatornáinak váltása című témakörben talál.](https://support.microsoft.com/help/3185078/how-to-switch-from-semi-annual-channel-to-monthly-channel)</span><span class="sxs-lookup"><span data-stu-id="e8ff4-121">For more information, see [How to switch update channels for existing Office Apps](https://support.microsoft.com/help/3185078/how-to-switch-from-semi-annual-channel-to-monthly-channel).</span></span> 

<span data-ttu-id="e8ff4-122">A felhasználók egy kiválasztott csoportjának frissítési csatornáinak váltásához vagy a Configuration Manager (SCCM) használatával konfigurálja a Csatorna frissítése beállítást a csoportházirend-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="e8ff4-122">For switching update channels for a selected group of users or by using Configuration Manager (SCCM), configure the Update Channel setting using GPO.</span></span> <span data-ttu-id="e8ff4-123">További információt a [Microsoft 365-alkalmazások frissítési csatornáinak áttekintése című témakörben talál.](https://docs.microsoft.com/deployoffice/overview-update-channels#group-policy)</span><span class="sxs-lookup"><span data-stu-id="e8ff4-123">For more info, see [Overview of update channels for Microsoft 365 Apps](https://docs.microsoft.com/deployoffice/overview-update-channels#group-policy).</span></span> <span data-ttu-id="e8ff4-124">További információt Az [Office 365 ProPlus-csatornák informatikai szakembereknek való kezelése](https://techcommunity.microsoft.com/t5/office-365-blog/how-to-manage-office-365-proplus-channels-for-it-pros/ba-p/795813) és a Microsoft [365-alkalmazások frissítéseinek kezelése a Microsoft Endpoint Configuration Manager rel.](https://docs.microsoft.com/deployoffice/manage-microsoft-365-apps-updates-configuration-manager)</span><span class="sxs-lookup"><span data-stu-id="e8ff4-124">For details, see [How to manage Office 365 ProPlus Channels for IT Pros](https://techcommunity.microsoft.com/t5/office-365-blog/how-to-manage-office-365-proplus-channels-for-it-pros/ba-p/795813) and [Manage updates to Microsoft 365 Apps with Microsoft Endpoint Configuration Manager](https://docs.microsoft.com/deployoffice/manage-microsoft-365-apps-updates-configuration-manager).</span></span>