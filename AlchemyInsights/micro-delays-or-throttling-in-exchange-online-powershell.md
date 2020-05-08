---
title: Mikrokésés és -szabályozás az Exchange Online PowerShellben
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Priority
ms.collection: Adm_O365
ms.custom:
- "3500011"
- "5106"
ms.openlocfilehash: 7ab4e7f18b7b8edf08098af8fe9674f66b1b81f4
ms.sourcegitcommit: fbaa2ce2cfb4d56d8c4cf2fa2d95489bdfcb7ff0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/30/2020
ms.locfileid: "43947911"
---
# <a name="micro-delays-or-throttling-in-exchange-online-powershell"></a><span data-ttu-id="151f0-102">Mikrokésés és -szabályozás az Exchange Online PowerShellben</span><span class="sxs-lookup"><span data-stu-id="151f0-102">Micro delays or throttling in Exchange Online PowerShell</span></span>

<span data-ttu-id="151f0-103">Amikor parancsfájlokat és parancsmagokat futtat az Exchange Online-ban, "mikrokésés alkalmazása" figyelmeztetések vagy késések léphetnek fel.</span><span class="sxs-lookup"><span data-stu-id="151f0-103">You might see "Micro delay applied" warnings or delays when you run scripts and cmdlets in Exchange Online.</span></span> <span data-ttu-id="151f0-104">Ezzel kapcsolatban íme két javaslat:</span><span class="sxs-lookup"><span data-stu-id="151f0-104">Here are two suggestions related to this:</span></span>

- <span data-ttu-id="151f0-105">Jobb megoldás lenne az [Exchange Online v2 PowerShell-modul](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2?view=exchange-ps) használata, amely a REST API-alapú parancsmagokat is tartalmazza, és lényegesen jobb teljesítményt nyújt.</span><span class="sxs-lookup"><span data-stu-id="151f0-105">You might want to try using the [Exchange Online v2 PowerShell module](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2?view=exchange-ps), which includes CMDlets that are based on REST API and are significantly more performant.</span></span> <span data-ttu-id="151f0-106">Ez nagyszerű megoldás lehet a gyakran használt beszerzési parancsmagok esetén.</span><span class="sxs-lookup"><span data-stu-id="151f0-106">This might be a great solution for a lot of Get- CMDlets that are frequently used.</span></span>
- <span data-ttu-id="151f0-107">Ha a v2 modulban nem szereplő parancsmagokat kell használnia, olvassa el a [PowerShell-parancsmagok használata nagy számú felhasználó esetén az Office 365-ben](https://techcommunity.microsoft.com/t5/exchange-team-blog/updated-running-powershell-cmdlets-for-large-numbers-of-users-in/ba-p/1000628#) című témakört, amelyből megtudhatja, hogy miként tájékozódhat az Exchange Online-ban várható PowerShell-szabályozási korlátozásokról.</span><span class="sxs-lookup"><span data-stu-id="151f0-107">If you need to use CMDlets that are not covered in the v2 module yet, please see [Running PowerShell cmdlets for large numbers of users in Office 365](https://techcommunity.microsoft.com/t5/exchange-team-blog/updated-running-powershell-cmdlets-for-large-numbers-of-users-in/ba-p/1000628#), which talks about how to get around expected PowerShell throttling limits in Exchange Online.</span></span>