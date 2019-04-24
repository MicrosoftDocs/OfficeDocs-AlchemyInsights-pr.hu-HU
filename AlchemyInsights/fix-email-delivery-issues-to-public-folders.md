---
title: E-mail kézbesítési javításokat üzenetet engedélyező nyilvános mappákhoz
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.custom: 1956
ms.assetid: ''
ms.openlocfilehash: 45665f900014c52e6a920325b0a3b0f6f79fb72d
ms.sourcegitcommit: d1c1d5bcb52ba9083e8dd7603feb72436c5154c8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/17/2019
ms.locfileid: "31910603"
---
# <a name="fix-email-delivery-issues-to-mail-enabled-public-folders"></a>E-mail kézbesítési javításokat üzenetet engedélyező nyilvános mappákhoz

Ha a külső feladóktól nem tudnak üzeneteket küldeni az üzenetet engedélyező nyilvános mappákat, és a feladók hibaüzenet: **nem található (550 5.4.1)**, ellenőrizze az e-mail tartomány számára a nyilvános mappát úgy van beállítva, egy belső továbbítási tartományként helyett egy a tartomány mérvadó:

1. Nyissa meg az [Exchange felügyeleti központ (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center).

2. Ugrás a **levelezés** \> **elfogadott tartományok**, jelölje ki az elfogadott tartomány, és kattintson a **Szerkesztés**.

3. Tulajdonságai lapon, hogy megnyílik, ha **mérvadó**a tartományban típusának beállítása, **belső továbbítási** módosítsa az értéket, és kattintson a **Mentés**.

Külső feladók **Nincs engedélye (550 5.7.13)** hiba jelenik meg, ha az [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) a nyilvános mappában a névtelen felhasználók engedélyeinek megtekintéséhez futtassa a következő parancsot:

`Get-PublicFolderClientPermission -Identity "<PublicFolderIdentity>" -User Anonymous`Például `Get-PublicFolderClientPermission -Identity "\Customer Discussion" -User Anonymous`.

A külső felhasználók e-mail küldése a nyilvános mappa, adja hozzá a CreateItems hozzáférés jobbra a névtelen felhasználó. Használja például a `Add-PublicFolderClientPermission -Identity "\Customer Discussion" -User Anonymous -AccessRights CreateItems` címet.