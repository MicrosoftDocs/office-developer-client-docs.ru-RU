---
title: RuleEnum (Справочник по для настольных баз данных Access)
TOCTitle: RuleEnum
ms:assetid: 5b59f202-315b-09b7-8505-9ac08ceccb3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249317(v=office.15)
ms:contentKeyID: 48545071
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: bac61333ab9d8c7abdbbb23a8207716f50c4ac21
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879096"
---
# <a name="ruleenum"></a><span data-ttu-id="eff74-102">RuleEnum</span><span class="sxs-lookup"><span data-stu-id="eff74-102">RuleEnum</span></span>

<span data-ttu-id="eff74-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eff74-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eff74-104">Задает правило, которое следует придерживаться при удалении [ключа](key-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="eff74-104">Specifies the rule to follow when a [Key](key-object-adox.md) is deleted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eff74-105">Константа</span><span class="sxs-lookup"><span data-stu-id="eff74-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="eff74-106">Значение</span><span class="sxs-lookup"><span data-stu-id="eff74-106">Value</span></span></p></th>
<th><p><span data-ttu-id="eff74-107">Описание</span><span class="sxs-lookup"><span data-stu-id="eff74-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eff74-108"><strong>adRICascade</strong></span><span class="sxs-lookup"><span data-stu-id="eff74-108"><strong>adRICascade</strong></span></span></p></td>
<td><p><span data-ttu-id="eff74-109">1</span><span class="sxs-lookup"><span data-stu-id="eff74-109">1</span></span></p></td>
<td><p><span data-ttu-id="eff74-110">Передавать изменения.</span><span class="sxs-lookup"><span data-stu-id="eff74-110">Cascade changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff74-111"><strong>adRINone</strong></span><span class="sxs-lookup"><span data-stu-id="eff74-111"><strong>adRINone</strong></span></span></p></td>
<td><p><span data-ttu-id="eff74-112">0</span><span class="sxs-lookup"><span data-stu-id="eff74-112">0</span></span></p></td>
<td><p><span data-ttu-id="eff74-113">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eff74-113">Default.</span></span> <span data-ttu-id="eff74-114">Никакие действия не предпринимаются.</span><span class="sxs-lookup"><span data-stu-id="eff74-114">No action is taken.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff74-115"><strong>adRISetDefault</strong></span><span class="sxs-lookup"><span data-stu-id="eff74-115"><strong>adRISetDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="eff74-116">3</span><span class="sxs-lookup"><span data-stu-id="eff74-116">3</span></span></p></td>
<td><p><span data-ttu-id="eff74-117">По умолчанию установлено значение внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="eff74-117">Foreign key value is set to the default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff74-118"><strong>adRISetNull</strong></span><span class="sxs-lookup"><span data-stu-id="eff74-118"><strong>adRISetNull</strong></span></span></p></td>
<td><p><span data-ttu-id="eff74-119">2</span><span class="sxs-lookup"><span data-stu-id="eff74-119">2</span></span></p></td>
<td><p><span data-ttu-id="eff74-120">Значение внешнего ключа задано значение null.</span><span class="sxs-lookup"><span data-stu-id="eff74-120">Foreign key value is set to null.</span></span></p></td>
</tr>
</tbody>
</table>

