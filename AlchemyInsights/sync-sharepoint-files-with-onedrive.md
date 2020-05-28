---
title: A Megnyitás Intézővel paranccsal kapcsolatos hibák elhárítása a SharePoint Online-ban
ms.author: pebaum
author: pebaum
manager: pamgreen
ms.date: 04/21/2020
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom: ''
ms.assetid: 5ad2f1f2-9650-4eb0-b4fa-2f52a09f535a
ms.openlocfilehash: be1136f7fd4575d482d38ee70163e5252d4ffbca
ms.sourcegitcommit: 5296874062b16f945d9a7a7a9ab29ec53686310b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/21/2020
ms.locfileid: "44343204"
---
# <a name="troubleshoot-open-with-explorer-issues-in-sharepoint-online"></a><span data-ttu-id="8c048-102">A Megnyitás Intézővel paranccsal kapcsolatos hibák elhárítása a SharePoint Online-ban</span><span class="sxs-lookup"><span data-stu-id="8c048-102">Troubleshoot “Open with Explorer” issues in SharePoint Online</span></span>

<span data-ttu-id="8c048-103">Azt javasoljuk, hogy [a SharePoint-fájlok szinkronizálását a OneDrive új szinkronizálási ügyfelével végezze el](https://support.office.com/article/sync-sharepoint-files-with-the-new-onedrive-sync-client-6de9ede8-5b6e-4503-80b2-6190f3354a88), amely az [Igény szerinti fájlok](https://support.office.com/article/learn-about-onedrive-files-on-demand-0e6860d3-d9f3-4971-b321-7092438fb38e) funkcióval helyi hozzáférést biztosít a fájlokhoz, és a legjobb teljesítményt nyújtja.</span><span class="sxs-lookup"><span data-stu-id="8c048-103">We recommend [syncing SharePoint files with the new OneDrive sync client](https://support.office.com/article/sync-sharepoint-files-with-the-new-onedrive-sync-client-6de9ede8-5b6e-4503-80b2-6190f3354a88) which provides [Files On-Demand](https://support.office.com/article/learn-about-onedrive-files-on-demand-0e6860d3-d9f3-4971-b321-7092438fb38e) because it provides local access to your files and offers the best performance.</span></span>

<span data-ttu-id="8c048-104">A Megnyitás Intézővel funkcióval kapcsolatos problémák elhárításához kövesse az alábbi cikkekben szereplő lépéseket és ajánlott eljárásokat:</span><span class="sxs-lookup"><span data-stu-id="8c048-104">To troubleshoot Open with Explorer issues, follow the steps and best practices in the following articles:</span></span>

- [<span data-ttu-id="8c048-105">A „Megnyitás Intézővel“ parancs használata a SharePoint Online-ban előforduló hibák elhárításához</span><span class="sxs-lookup"><span data-stu-id="8c048-105">How to use the "Open with Explorer" command to troubleshoot issues in SharePoint Online</span></span>](https://docs.microsoft.com/sharepoint/support/lists-and-libraries/troubleshoot-issues-using-open-with-explorer)
- [<span data-ttu-id="8c048-106">Tárban lévő fájlok másolása vagy áthelyezése a Megnyitás Intézővel parancs használatával</span><span class="sxs-lookup"><span data-stu-id="8c048-106">Copy or move library files by using Open with Explorer</span></span>](https://support.office.com/article/copy-or-move-library-files-by-using-open-with-explorer-aaee7bfb-e2a1-42ee-8fc0-bcc0754f04d2)

> <span data-ttu-id="8c048-107">**Megjegyzés:**</span><span class="sxs-lookup"><span data-stu-id="8c048-107">**Note:**</span></span>
>- <span data-ttu-id="8c048-108">A Megnyitás Intézővel funkció csak az Internet Explorer 10-es és 11-es verziójában támogatott.</span><span class="sxs-lookup"><span data-stu-id="8c048-108">Open with Explorer is only supported in Internet Explorer 10 or 11.</span></span> <span data-ttu-id="8c048-109">A Megnyitás Intézővel parancs nem használható a Windowsban a Microsoft Edge, a Google Chrome, a Mozilla Firefox böngészővel, illetve a Mac platformon.</span><span class="sxs-lookup"><span data-stu-id="8c048-109">Open with Explorer doesn't work in Windows with Microsoft Edge, Google Chrome, Mozilla Firefox, or on the Mac platform.</span></span> <span data-ttu-id="8c048-110">Emiatt előfordulhat, hogy a Tallózó nézet beállítás szürkén jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="8c048-110">Due to this reason, the Explorer View option may be grayed out.</span></span>
>
>- <span data-ttu-id="8c048-111">A Megnyitás Intézővel gomb nem jelenik meg a tár új felületén.</span><span class="sxs-lookup"><span data-stu-id="8c048-111">The Open with Explorer button doesn't appear in the new library experience.</span></span> <span data-ttu-id="8c048-112">Kattintson a jobb felső sarokban lévő **Nézet** legördülő menüre (a legördülő menü neve az aktuális nézettől függően változik), majd válassza a **Megtekintés Fájlkezelőben elemet**.</span><span class="sxs-lookup"><span data-stu-id="8c048-112">Select the **View** drop-down in the upper right (the name of the drop-down changes depending on your current view), and then select **View in File Explorer**.</span></span>
