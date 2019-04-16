---
title: A SharePoint, a OneDrive és a csapatok a Microsoft Office 365 ATP engedélyezése
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 04/01/2019
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Admin_O365
ms.custom: 3100021
ms.openlocfilehash: ae2f574663ae3233a056589c2d5a578171f3b2f4
ms.sourcegitcommit: 601aec31e6556286fe5e0fd62827a037cbb6fe17
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030990"
---
# <a name="enable-office-365-advanced-threat-protection-for-sharepoint-online-onedrive-and-microsoft-teams"></a><span data-ttu-id="1e206-102">SharePoint Online, a OneDrive és a csapatok a Microsoft Office 365 speciális fenyegetés védelem engedélyezése</span><span class="sxs-lookup"><span data-stu-id="1e206-102">Enable Office 365 Advanced Threat Protection for SharePoint Online, OneDrive, and Microsoft Teams</span></span>

1. <span data-ttu-id="1e206-103">Ugrás a https://protection.office.com és jelentkezzen be.</span><span class="sxs-lookup"><span data-stu-id="1e206-103">Go to https://protection.office.com and sign in.</span></span>
2. <span data-ttu-id="1e206-104">Válassza ki a **fenyegetés kezelése** > **politika** > **Biztonságos mellékletek**.</span><span class="sxs-lookup"><span data-stu-id="1e206-104">Choose **Threat management** > **Policy** > **Safe Attachments**.</span></span>
3. <span data-ttu-id="1e206-105">Válassza az **Ígérethez rendelkezésre álló mennyiség, a SharePoint, a OneDrive, és a Microsoft csapatok**, és kattintson a **Mentés**gombra.</span><span class="sxs-lookup"><span data-stu-id="1e206-105">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**, and then click **Save**.</span></span>
4. <span data-ttu-id="1e206-106">(Ajánlott) A globális rendszergazda vagy a SharePoint Online rendszergazdaként futtassa a [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps) parancsmaggal a **DisallowInfectedFileDownload** paraméter értéke *true*.</span><span class="sxs-lookup"><span data-stu-id="1e206-106">(Recommended) As a global administrator or a SharePoint Online administrator, run the [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps) cmdlet with the **DisallowInfectedFileDownload** parameter set to *true*.</span></span>
5. <span data-ttu-id="1e206-107">(Ajánlott) [Értesítések beállítása](https://docs.microsoft.com/office365/securitycompliance/turn-on-atp-for-spo-odb-and-teams#set-up-alerts-for-detected-files) a talált fájlokat.</span><span class="sxs-lookup"><span data-stu-id="1e206-107">(Recommended) [Set up alerts](https://docs.microsoft.com/office365/securitycompliance/turn-on-atp-for-spo-odb-and-teams#set-up-alerts-for-detected-files) for detected files.</span></span>

> [!NOTE]
> <span data-ttu-id="1e206-108">ATP lesz nto vizsgálat minden SharePoint Online, a OneDrive vagy a Microsoft Teams egyetlen fájlban.</span><span class="sxs-lookup"><span data-stu-id="1e206-108">ATP will nto scan every single file in SharePoint Online, OneDrive, or Microsoft Teams.</span></span> <span data-ttu-id="1e206-109">Fájlok megosztása és a Vendég tevékenység események, intelligens heurisztikus és rosszindulatú fájlok azonosítása veszély jelek használó folyamat aszinkron módon ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="1e206-109">Files are scanned asynchronously, through a process that uses sharing and guest activity events, along with smart heuristics and threat signals to identify malicious files.</span></span> <span data-ttu-id="1e206-110">Lásd: [https://docs.microsoft.com/office365/securitycompliance/atp-for-spo-odb-and-teams](https://docs.microsoft.com/office365/securitycompliance/atp-for-spo-odb-and-teams).</span><span class="sxs-lookup"><span data-stu-id="1e206-110">See [https://docs.microsoft.com/office365/securitycompliance/atp-for-spo-odb-and-teams](https://docs.microsoft.com/office365/securitycompliance/atp-for-spo-odb-and-teams).</span></span>