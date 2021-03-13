---
title: A felhasználói házirend/postaláda beállításainak kijavítva
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
ms.openlocfilehash: ca998c453fcb0905b122436f0eea384a9b8a9992
ms.sourcegitcommit: 6312ee31561db36104f32282d019d069ede69174
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/11/2021
ms.locfileid: "50746729"
---
# <a name="fix-user-policymailbox-settings"></a><span data-ttu-id="0fa22-102">A felhasználói házirend/postaláda beállításainak kijavítva</span><span class="sxs-lookup"><span data-stu-id="0fa22-102">Fix user policy/mailbox settings</span></span>

<span data-ttu-id="0fa22-103">A postaláda levélszemét-beállításai érintették ezt az üzenetet.</span><span class="sxs-lookup"><span data-stu-id="0fa22-103">The junk mail settings on the mailbox affected this message.</span></span> <span data-ttu-id="0fa22-104">A beállítások áttekintéséhez tegye a következőket:</span><span class="sxs-lookup"><span data-stu-id="0fa22-104">To review the settings, do the following:</span></span>

1. <span data-ttu-id="0fa22-105">Indítsa el az Exchange Management Shellt.</span><span class="sxs-lookup"><span data-stu-id="0fa22-105">Launch Exchange Management Shell.</span></span> <span data-ttu-id="0fa22-106">További információ: [Az Exchange Management Shell megnyitása.](https://go.microsoft.com/fwlink/?linkid=2101432)</span><span class="sxs-lookup"><span data-stu-id="0fa22-106">For more information, see [Open the Exchange Management Shell](https://go.microsoft.com/fwlink/?linkid=2101432).</span></span>
2. <span data-ttu-id="0fa22-107">Futtassa ezt a parancsot (a felhasználó  **e-mail-címével): get-mailboxjunkmailconfiguration -identity "user@domain.com"**</span><span class="sxs-lookup"><span data-stu-id="0fa22-107">Run this command (using the user's email address):  **get-mailboxjunkmailconfiguration -identity "user@domain.com"**</span></span>
3. <span data-ttu-id="0fa22-108">Ellenőrizze, hogy a feladó e-mail-címe **TrustedSendersAndDomains** vagy **BlockedSendersAndDomains tartomány részét képezi-e.**</span><span class="sxs-lookup"><span data-stu-id="0fa22-108">Check if the sender's email address is part of **TrustedSendersAndDomains** or **BlockedSendersAndDomains**.</span></span> <span data-ttu-id="0fa22-109">Ha az e-mail-cím a listák egyikében található, előfordulhat, hogy el kell távolítania.</span><span class="sxs-lookup"><span data-stu-id="0fa22-109">If the email address is in one of the lists, you may have to remove it.</span></span> <span data-ttu-id="0fa22-110">További információ: [Set-MailboxJunkEmailConfiguration](https://go.microsoft.com/fwlink/?linkid=2101047).</span><span class="sxs-lookup"><span data-stu-id="0fa22-110">To learn more, see [Set-MailboxJunkEmailConfiguration](https://go.microsoft.com/fwlink/?linkid=2101047).</span></span>