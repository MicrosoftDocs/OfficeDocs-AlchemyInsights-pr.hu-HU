---
title: A feltételes hozzáférés használata az Intune-nal
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
- "6700002"
- "7680"
ms.openlocfilehash: 6e86c6b4c9c6adcbeac504acd5a10f2139d04237
ms.sourcegitcommit: 475a9eaa095812091991857df6cf6490a8bbe179
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/08/2021
ms.locfileid: "50693577"
---
# <a name="using-conditional-access-with-intune"></a><span data-ttu-id="f5d6a-102">A feltételes hozzáférés használata az Intune-nal</span><span class="sxs-lookup"><span data-stu-id="f5d6a-102">Using Conditional Access with Intune</span></span>

<span data-ttu-id="f5d6a-103">A feltételes hozzáférés Intune-nal való használatához 3 lépés szükséges:</span><span class="sxs-lookup"><span data-stu-id="f5d6a-103">Using Conditional Access with Intune requires 3 steps:</span></span>

- [<span data-ttu-id="f5d6a-104">Hozzon létre megfelelőségi szabályzatot az eszköz megfelelőnek minősülő beállításainak meghatározásához. Egy eszköznek például legalább 6 jegyű pin-kódot kell lennie, mielőtt megfelelőnek minősül.</span><span class="sxs-lookup"><span data-stu-id="f5d6a-104">Create a Compliance Policy to define settings that must be met before the device is considered compliant. For example, a device must have a pin of at least 6 digits before it is considered compliant.</span></span>](https://docs.microsoft.com/mem/intune/protect/create-compliance-policy)
- [<span data-ttu-id="f5d6a-105">Hozzon létre egy feltételes hozzáférési házirendet, amely meghatározza, hogy milyen erőforrások vannak védve, és milyen feltételeknek kell teljesülni az erőforrások eléréséhez. Egy eszköznek például kompatibilisnek kell lennie a vállalati e-mailek elérése előtt.</span><span class="sxs-lookup"><span data-stu-id="f5d6a-105">Create a Conditional Access Policy that defines what resources are being protected, and what conditions need to be met to access those resources. For example, a device must be compliant before accessing corporate email.</span></span>](https://docs.microsoft.com/mem/intune/protect/tutorial-protect-email-on-unmanaged-devices#create-conditional-access-policies)
- [<span data-ttu-id="f5d6a-106">Győződjön meg arról, hogy a megfelelőségi szabályzatok és a feltételes hozzáférési szabályzatok a kívánt felhasználócsoportokra vannak megcélzottak. Ehhez szükség lehet bizonyos felhasználói csoportok létrehozására az Azure Active Directoryban.</span><span class="sxs-lookup"><span data-stu-id="f5d6a-106">Ensure both Compliance Policies and Conditional Access Policies are targeted to the desired groups of users. This may require creating specific groups of users in Azure Active Directory.</span></span>](https://docs.microsoft.com/troubleshoot/mem/intune/troubleshoot-conditional-access)

[<span data-ttu-id="f5d6a-107">További tudnivalók...</span><span class="sxs-lookup"><span data-stu-id="f5d6a-107">Read more...</span></span>](https://docs.microsoft.com/mem/intune/protect/device-compliance-get-started)