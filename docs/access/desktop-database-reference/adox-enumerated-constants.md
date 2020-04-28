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
# <a name="adox-enumerated-constants"></a><span data-ttu-id="3702e-102">Перечислимые константы ADOX</span><span class="sxs-lookup"><span data-stu-id="3702e-102">ADOX enumerated constants</span></span>

<span data-ttu-id="3702e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3702e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3702e-104">Для поддержки отладки в списке константы ADOX перечислены значения для каждой константы.</span><span class="sxs-lookup"><span data-stu-id="3702e-104">To assist debugging, the ADOX enumerated constants list a value for each constant.</span></span> <span data-ttu-id="3702e-105">Однако это значение является исключительно рекомендацией и может изменяться от одного выпуска ADOX к другому.</span><span class="sxs-lookup"><span data-stu-id="3702e-105">However, this value is purely advisory, and may change from one release of ADOX to another.</span></span> <span data-ttu-id="3702e-106">Код должен зависеть только от имени, а не фактического значения перечислимых констант.</span><span class="sxs-lookup"><span data-stu-id="3702e-106">Your code should only depend on the name, not the actual value, of enumerated constants.</span></span>

<span data-ttu-id="3702e-107">Определены следующие перечислимые константы.</span><span class="sxs-lookup"><span data-stu-id="3702e-107">The following enumerated constants are defined.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3702e-108">Перечисление</span><span class="sxs-lookup"><span data-stu-id="3702e-108">Enumeration</span></span></p></th>
<th><p><span data-ttu-id="3702e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3702e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3702e-110"><a href="actionenum.md">ActionEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-110"><a href="actionenum.md">ActionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-111">Задает тип действия, выполняемого при вызове <strong>SetPermissions</strong> .</span><span class="sxs-lookup"><span data-stu-id="3702e-111">Specifies the type of action to be performed when <strong>SetPermissions</strong> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3702e-112"><a href="allownullsenum.md">AllowNullsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-112"><a href="allownullsenum.md">AllowNullsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-113">Указывает, индексируются ли записи со значениями NULL.</span><span class="sxs-lookup"><span data-stu-id="3702e-113">Specifies whether records with null values are indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3702e-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-115">Задает характеристики <strong>столбца</strong>.</span><span class="sxs-lookup"><span data-stu-id="3702e-115">Specifies characteristics of a <strong>Column</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3702e-116"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-116"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-117">Указывает тип данных <strong>поля</strong>, <strong>параметра</strong>или <strong>Свойства</strong>.</span><span class="sxs-lookup"><span data-stu-id="3702e-117">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3702e-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-119">Указывает, как объекты наследуют разрешения, заданные с помощью <strong>SetPermissions</strong>.</span><span class="sxs-lookup"><span data-stu-id="3702e-119">Specifies how objects will inherit permissions set with <strong>SetPermissions</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3702e-120"><a href="keytypeenum.md">KeyTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-120"><a href="keytypeenum.md">KeyTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-121">Указывает тип <strong>ключа</strong>: основной, внешний или уникальный.</span><span class="sxs-lookup"><span data-stu-id="3702e-121">Specifies the type of <strong>Key</strong>: primary, foreign, or unique.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3702e-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-123">Указывает тип объекта базы данных, для которого необходимо задать разрешения или владельца.</span><span class="sxs-lookup"><span data-stu-id="3702e-123">Specifies the type of database object for which to set permissions or ownership.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3702e-124"><a href="rightsenum.md">RightsEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-124"><a href="rightsenum.md">RightsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-125">Задает права или разрешения для группы или пользователя в объекте.</span><span class="sxs-lookup"><span data-stu-id="3702e-125">Specifies the rights or permissions for a group or user on an object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3702e-126"><a href="ruleenum.md">RuleEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-126"><a href="ruleenum.md">RuleEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-127">Задает правило, которое необходимо выполнить при удалении <strong>ключа</strong> .</span><span class="sxs-lookup"><span data-stu-id="3702e-127">Specifies the rule to follow when a <strong>Key</strong> is deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3702e-128"><a href="sortorderenum.md">SortOrderEnum</a></span><span class="sxs-lookup"><span data-stu-id="3702e-128"><a href="sortorderenum.md">SortOrderEnum</a></span></span></p></td>
<td><p><span data-ttu-id="3702e-129">Задает последовательность сортировки для индексированного столбца.</span><span class="sxs-lookup"><span data-stu-id="3702e-129">Specifies the sort sequence for an indexed column.</span></span></p></td>
</tr>
</tbody>
</table>

