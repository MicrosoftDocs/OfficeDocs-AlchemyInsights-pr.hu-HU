---
title: 1048 5.7.750 Szolgáltatás nem érhető el. Az ügyfél nem regisztrált tartományokból nem küldhető el
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: 04/21/2020
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.assetid: 8cf6d70b-9a78-4f04-ac59-7ffcf44ffd22
ms.custom:
- "1048"
- "3100026"
ms.openlocfilehash: 48b9c2de27f8d7f52215c3a3d547bdf746a3a4cd
ms.sourcegitcommit: 55eff703a17e500681d8fa6a87eb067019ade3cc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/22/2020
ms.locfileid: "43676715"
---
# <a name="57750-client-blocked-from-sending-from-unregistered-domain"></a><span data-ttu-id="dfa57-103">5.7.750 Ügyfél letiltotta a küldés nem regisztrált domain</span><span class="sxs-lookup"><span data-stu-id="dfa57-103">5.7.750 Client blocked from sending from unregistered domain</span></span>

<span data-ttu-id="dfa57-104">A hiba akkor fordul elő, ha nagy mennyiségű üzenetet küldenek olyan tartományokból, amelyek nincsenek kiépítve a bérlőben (elfogadott tartományként hozzáadva és érvényesítve).</span><span class="sxs-lookup"><span data-stu-id="dfa57-104">The error occurs when a large volume of messages are sent from domains that aren't provisioned in your tenant (added as accepted domains and validated).</span></span>

<span data-ttu-id="dfa57-105">A hiba elkerülése érdekében használhat egy tanúsítványalapú levélfolyam-összekötőt, ahol a tanúsítvány tartománya kiépített tartomány, vagy kiépítheti az összes küldő tartományt.</span><span class="sxs-lookup"><span data-stu-id="dfa57-105">To avoid this error, you can use a certificate-based mail flow connector where the certificate's domain is a provisioned domain, or you can provision all sending domains.</span></span>
