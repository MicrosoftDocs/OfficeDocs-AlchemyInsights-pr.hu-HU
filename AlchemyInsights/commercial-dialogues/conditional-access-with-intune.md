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
ms.sourcegitcommit: 6312ee31561db36104f32282d019d069ede69174
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/11/2021
ms.locfileid: "50746029"
---
# <a name="using-conditional-access-with-intune"></a><span data-ttu-id="f8ff5-102">A feltételes hozzáférés használata az Intune-nal</span><span class="sxs-lookup"><span data-stu-id="f8ff5-102">Using Conditional Access with Intune</span></span>

<span data-ttu-id="f8ff5-103">A feltételes hozzáférés Intune-nal való használata 3 lépést igényel:</span><span class="sxs-lookup"><span data-stu-id="f8ff5-103">Using Conditional Access with Intune requires 3 steps:</span></span>

- [<span data-ttu-id="f8ff5-104">Hozzon létre egy megfelelőségi szabályzatot, amely meghatározza azokat a beállításokat, amelyeknek meg kell felelnie ahhoz, hogy az eszköz megfelelőnek minősül. Egy eszköznek például legalább 6 számjegyű PIN-kódot kell kitűznie, mielőtt megfelelőnek minősül.</span><span class="sxs-lookup"><span data-stu-id="f8ff5-104">Create a Compliance Policy to define settings that must be met before the device is considered compliant. For example, a device must have a pin of at least 6 digits before it is considered compliant.</span></span>](https://docs.microsoft.com/mem/intune/protect/create-compliance-policy)
- [<span data-ttu-id="f8ff5-105">Hozzon létre egy feltételes hozzáférési házirendet, amely meghatározza a védett erőforrásokat és az erőforrások eléréséhez szükséges feltételeket. Egy eszköznek például kompatibilisnek kell lennie a vállalati e-mailek elérése előtt.</span><span class="sxs-lookup"><span data-stu-id="f8ff5-105">Create a Conditional Access Policy that defines what resources are being protected, and what conditions need to be met to access those resources. For example, a device must be compliant before accessing corporate email.</span></span>](https://docs.microsoft.com/mem/intune/protect/tutorial-protect-email-on-unmanaged-devices#create-conditional-access-policies)
- [<span data-ttu-id="f8ff5-106">Győződjön meg arról, hogy a megfelelőségi szabályzatok és a feltételes hozzáférési szabályzatok a kívánt felhasználócsoportokra vannak megcélzottak. Ehhez szükség lehet arra, hogy felhasználócsoportokat hozzon létre az Azure Active Directoryban.</span><span class="sxs-lookup"><span data-stu-id="f8ff5-106">Ensure both Compliance Policies and Conditional Access Policies are targeted to the desired groups of users. This may require creating specific groups of users in Azure Active Directory.</span></span>](https://docs.microsoft.com/troubleshoot/mem/intune/troubleshoot-conditional-access)

[<span data-ttu-id="f8ff5-107">További tudnivalók...</span><span class="sxs-lookup"><span data-stu-id="f8ff5-107">Read more...</span></span>](https://docs.microsoft.com/mem/intune/protect/device-compliance-get-started)