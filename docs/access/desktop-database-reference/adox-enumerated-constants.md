---
title: Перечислимые константы ADOX
TOCTitle: ADOX enumerated constants
ms:assetid: 0ad716a0-8801-50cb-024a-85c308c65c78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248840(v=office.15)
ms:contentKeyID: 48543163
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 385a3a106c04db11b36ea646368f80fe28ffd413
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280197"
---
# <a name="adox-enumerated-constants"></a><span data-ttu-id="e8c4c-102">Перечислимые константы ADOX</span><span class="sxs-lookup"><span data-stu-id="e8c4c-102">ADOX enumerated constants</span></span>

<span data-ttu-id="e8c4c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8c4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8c4c-104">Для отладки перечислимые константы ADOX перечисляют значение для каждой константы.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-104">To assist debugging, the ADOX enumerated constants list a value for each constant.</span></span> <span data-ttu-id="e8c4c-105">Однако это значение является исключительно рекомендациями и может измениться с одного выпуска ADOX на другой.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-105">However, this value is purely advisory, and may change from one release of ADOX to another.</span></span> <span data-ttu-id="e8c4c-106">Ваш код должен зависеть только от имени, а не фактического значения, а от суммированных констант.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-106">Your code should only depend on the name, not the actual value, of enumerated constants.</span></span>

<span data-ttu-id="e8c4c-107">Определены следующие константы с перемежением.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-107">The following enumerated constants are defined.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8c4c-108">Перечисление</span><span class="sxs-lookup"><span data-stu-id="e8c4c-108">Enumeration</span></span></p></th>
<th><p><span data-ttu-id="e8c4c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e8c4c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8c4c-110"><a href="actionenum.md">ActionEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-110"><a href="actionenum.md">ActionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-111">Указывает тип действия, выполняемого при выполнении <strong>действия SetPermissions.</strong></span><span class="sxs-lookup"><span data-stu-id="e8c4c-111">Specifies the type of action to be performed when <strong>SetPermissions</strong> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8c4c-112"><a href="allownullsenum.md">AllowNullsEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-112"><a href="allownullsenum.md">AllowNullsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-113">Указывает, индексироваться ли записи со значениями NULL.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-113">Specifies whether records with null values are indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8c4c-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-115">Указывает характеристики <strong>столбца.</strong></span><span class="sxs-lookup"><span data-stu-id="e8c4c-115">Specifies characteristics of a <strong>Column</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8c4c-116"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-116"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-117">Указывает тип данных <strong>поля,</strong> <strong>параметра</strong>или <strong>свойства.</strong></span><span class="sxs-lookup"><span data-stu-id="e8c4c-117">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8c4c-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-119">Указывает, как объекты наследуют разрешения, заданные с <strong>помощью SetPermissions.</strong></span><span class="sxs-lookup"><span data-stu-id="e8c4c-119">Specifies how objects will inherit permissions set with <strong>SetPermissions</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8c4c-120"><a href="keytypeenum.md">KeyTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-120"><a href="keytypeenum.md">KeyTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-121">Указывает тип key: <strong>primary,</strong>foreign или unique.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-121">Specifies the type of <strong>Key</strong>: primary, foreign, or unique.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8c4c-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-123">Указывает тип объекта базы данных, для которого необходимо установить разрешения или права владельца.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-123">Specifies the type of database object for which to set permissions or ownership.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8c4c-124"><a href="rightsenum.md">RightsEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-124"><a href="rightsenum.md">RightsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-125">Указывает права или разрешения для группы или пользователя объекта.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-125">Specifies the rights or permissions for a group or user on an object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8c4c-126"><a href="ruleenum.md">RuleEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-126"><a href="ruleenum.md">RuleEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-127">Правило, заданное при <strong>удалении</strong> ключа.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-127">Specifies the rule to follow when a <strong>Key</strong> is deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8c4c-128"><a href="sortorderenum.md">SortOrderEnum</a></span><span class="sxs-lookup"><span data-stu-id="e8c4c-128"><a href="sortorderenum.md">SortOrderEnum</a></span></span></p></td>
<td><p><span data-ttu-id="e8c4c-129">Указывает последовательность сортировки для индексного столбца.</span><span class="sxs-lookup"><span data-stu-id="e8c4c-129">Specifies the sort sequence for an indexed column.</span></span></p></td>
</tr>
</tbody>
</table>

