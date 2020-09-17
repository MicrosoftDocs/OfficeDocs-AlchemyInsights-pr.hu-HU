---
title: Törölt nyilvános mappa visszaállítása
ms.author: pebaum
author: pebaum
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- "3500007"
- "3488"
ms.openlocfilehash: bb7fe248714e9a7e7f4c48913b159b5c23132192
ms.sourcegitcommit: c6692ce0fa1358ec3529e59ca0ecdfdea4cdc759
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/15/2020
ms.locfileid: "47774533"
---
# <a name="restore-a-deleted-public-folder"></a>Törölt nyilvános mappa visszaállítása

**Törölt elemek visszaállítása nyilvános mappából**:

- Lásd: nem lehet [törölt elemeket visszaállítani egy nem levelezési nyilvános mappából az Outlook 2016](https://aka.ms/pfrec).
 
**Törölt nyilvános mappa (bármilyen típus) visszaállítása**: 

- Kérjük, használja az EXO PowerShell következő parancsát:

    Szintaxisa

     `$pf=Get-PublicFolder \NON_IPM_SUBTREE\DUMPSTER_ROOT -Recurse  | ?{$_.Name -eq "\<name_of_deleted_public_Folder"};Set-PublicFolder $pf.identity -Path \<path where the folder will be restored>`

    Példa: a következő parancs visszaállítja a Subfolder1-ot, és a \Parent1 alá helyezi:

    `$pf=Get-PublicFolder \NON_IPM_SUBTREE\DUMPSTER_ROOT -Recurse | ?{$_.Name -eq "Subfolder1"};Set-PublicFolder $pf.identity -Path \Parent1`

További információt a [törölt nyilvános mappa visszaállítása](https://docs.microsoft.com/exchange/collaboration-exo/public-folders/restore-deleted-public-folder) című témakörben talál.
