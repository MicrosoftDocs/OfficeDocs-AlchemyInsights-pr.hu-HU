---
title: Kivételek konfigurálása és érvényesítése az MDATP-hez Linux rendszerű gépeken
ms.author: v-jmathew
author: v-jmathew
manager: dansimp
audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- "9000760"
- "7391"
ms.openlocfilehash: 4fad0a513f7c6d2f0337019488a4055c25e1650d
ms.sourcegitcommit: 6312ee31561db36104f32282d019d069ede69174
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/11/2021
ms.locfileid: "50746022"
---
# <a name="configure-and-validate-exclusions-for-mdatp-on-a-linux-machine"></a><span data-ttu-id="f7a97-102">Kivételek konfigurálása és érvényesítése az MDATP-hez Linux rendszerű gépeken</span><span class="sxs-lookup"><span data-stu-id="f7a97-102">Configure and validate exclusions for MDATP on a Linux machine</span></span>

<span data-ttu-id="f7a97-103">Az MDATP-be való beolvasásból kizárhat bizonyos fájlokat, mappákat, folyamatokat és folyamat által megnyitott fájlokat.</span><span class="sxs-lookup"><span data-stu-id="f7a97-103">You can exclude certain files, folders, processes, and process-opened files from MDATP scans.</span></span> <span data-ttu-id="f7a97-104">A kivételek segítenek megelőzni a szoftverek és fájlok szervezeten belül egyedi vagy testre szabott észlelését.</span><span class="sxs-lookup"><span data-stu-id="f7a97-104">Exclusions help prevent incorrect detection of software and files unique or customized to your organization.</span></span> <span data-ttu-id="f7a97-105">A kizárások segítenek az MDATP által okozott teljesítményproblémák csökkentésében is.</span><span class="sxs-lookup"><span data-stu-id="f7a97-105">Exclusions also help mitigate performance problems caused by MDATP.</span></span>

<span data-ttu-id="f7a97-106">További információ: Kivételek konfigurálása és érvényesítése Linux [MDATP-hez.](https://go.microsoft.com/fwlink/?linkid=2144517)</span><span class="sxs-lookup"><span data-stu-id="f7a97-106">To learn more, see [Configure and validate exclusions for MDATP for Linux](https://go.microsoft.com/fwlink/?linkid=2144517).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7a97-107">A cikkben ismertetett kivételek nem vonatkoznak a Linux MDATP egyéb funkcióira, beleértve a végpontok észlelését és válaszát (EDR).</span><span class="sxs-lookup"><span data-stu-id="f7a97-107">The exclusions described in this article don't apply to other capabilities of MDATP for Linux, including endpoint detection and response (EDR).</span></span> <span data-ttu-id="f7a97-108">A cikkben ismertetett módszerekkel kizárt fájlok továbbra is kiválthatják az EDR-riasztásokat és más észlelési funkciókat.</span><span class="sxs-lookup"><span data-stu-id="f7a97-108">Files that you exclude by using the methods described in this article can still trigger EDR alerts and other detection capabilities.</span></span>