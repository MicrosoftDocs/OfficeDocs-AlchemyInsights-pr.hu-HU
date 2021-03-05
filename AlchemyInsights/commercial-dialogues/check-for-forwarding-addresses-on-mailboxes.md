---
title: A postaládák továbbítási címének ellenőrzése
ms.author: v-aiyengar
author: AshaIyengar21
manager: dansimp
ms.date: 17/02/2021
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- "9002486"
- "7524"
ms.openlocfilehash: 1b0a6c8fe368196f2d1f9811aea895c2c024b2e6
ms.sourcegitcommit: 251e2e82571fb3bb1fbe3dbf7bfca30e004b3373
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/05/2021
ms.locfileid: "50482773"
---
# <a name="check-for-forwarding-addresses-on-mailboxes"></a><span data-ttu-id="a327f-102">A postaládák továbbítási címének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="a327f-102">Check for forwarding addresses on mailboxes</span></span>

<span data-ttu-id="a327f-103">Néha a támadók saját magukra továbbítják a felhasználók e-mailjeit, ezért először ellenőrizzük, hogy vannak-e továbbítási címek és szabályok a postaládában.</span><span class="sxs-lookup"><span data-stu-id="a327f-103">Sometimes hackers forward users' email messages to themselves, so first we'll check for forwarding addresses and rules on the mailbox.</span></span> <span data-ttu-id="a327f-104">Ezután ellenőrizzük a naplókat.</span><span class="sxs-lookup"><span data-stu-id="a327f-104">Then we'll check the audit logs.</span></span> <span data-ttu-id="a327f-105">A következő lépésekkel ellenőrizheti a továbbítási címeket:</span><span class="sxs-lookup"><span data-stu-id="a327f-105">Here's how to check for forwarding addresses:</span></span>

1. <span data-ttu-id="a327f-106">Válassza **a Felhasználók aktív** felhasználók  >  **lehetőséget.**</span><span class="sxs-lookup"><span data-stu-id="a327f-106">Select **Users** > **Active users**.</span></span>
1. <span data-ttu-id="a327f-107">Jelölje ki azt a felhasználót, akinek a fiókját feltörték.</span><span class="sxs-lookup"><span data-stu-id="a327f-107">Select the user whose account has been compromised.</span></span>
1. <span data-ttu-id="a327f-108">A megjelenő előtűnésben bontsa ki a Levelezési **beállításokat,** majd kattintson a Szerkesztés  **e-mail-továbbításhoz elemre.**</span><span class="sxs-lookup"><span data-stu-id="a327f-108">In the flyout that appears, expand **Mail Settings**, and then click **Edit** for **Email forwarding**.</span></span>
1. <span data-ttu-id="a327f-109">Távolítsa el a nem felismert továbbítási címeket.</span><span class="sxs-lookup"><span data-stu-id="a327f-109">Remove any forwarding addresses you don't recognize.</span></span>