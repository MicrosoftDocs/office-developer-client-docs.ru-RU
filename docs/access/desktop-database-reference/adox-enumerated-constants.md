---
title: Перечислимые константы ADOX
TOCTitle: ADOX Enumerated Constants
ms:assetid: 0ad716a0-8801-50cb-024a-85c308c65c78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248840(v=office.15)
ms:contentKeyID: 48543163
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f8be72ea28d9814890bcaf193c1175725fcfe1d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869501"
---
# <a name="adox-enumerated-constants"></a><span data-ttu-id="ab2cd-102">Перечислимые константы ADOX</span><span class="sxs-lookup"><span data-stu-id="ab2cd-102">ADOX Enumerated Constants</span></span>


<span data-ttu-id="ab2cd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab2cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab2cd-104">Для помощи отладки, констант перечисления ADOX списка значение для каждого константу.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-104">To assist debugging, the ADOX enumerated constants list a value for each constant.</span></span> <span data-ttu-id="ab2cd-105">Тем не менее это значение исключительно рекомендации и может измениться в разных выпусках ADOX в другую.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-105">However, this value is purely advisory, and may change from one release of ADOX to another.</span></span> <span data-ttu-id="ab2cd-106">Код только должен зависеть от имени, а не фактические значения, перечисленных констант.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-106">Your code should only depend on the name, not the actual value, of enumerated constants.</span></span>

<span data-ttu-id="ab2cd-107">Следующие перечисляемые константы определены.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-107">The following enumerated constants are defined.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab2cd-108">Перечисление</span><span class="sxs-lookup"><span data-stu-id="ab2cd-108">Enumeration</span></span></p></th>
<th><p><span data-ttu-id="ab2cd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ab2cd-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab2cd-110"><a href="actionenum.md">ActionEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-110"><a href="actionenum.md">ActionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-111">Указывает тип действие, которое необходимо выполнить при вызове <strong>SetPermissions</strong> .</span><span class="sxs-lookup"><span data-stu-id="ab2cd-111">Specifies the type of action to be performed when <strong>SetPermissions</strong> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab2cd-112"><a href="allownullsenum.md">AllowNullsEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-112"><a href="allownullsenum.md">AllowNullsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-113">Указывает, индексированные записи с пустым значением.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-113">Specifies whether records with null values are indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab2cd-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-115">Определяет характеристики <strong>столбца</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-115">Specifies characteristics of a <strong>Column</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab2cd-116"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-116"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-117">Указывает тип данных <strong>параметра</strong>, <strong>поля</strong>или <strong>Свойства</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-117">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab2cd-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-119">Указывает, как будет наследуют разрешения, установленные с <strong>SetPermissions</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-119">Specifies how objects will inherit permissions set with <strong>SetPermissions</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab2cd-120"><a href="keytypeenum.md">KeyTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-120"><a href="keytypeenum.md">KeyTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-121">Указывает тип <strong>ключа</strong>: основной, внешний или уникальным.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-121">Specifies the type of <strong>Key</strong>: primary, foreign, or unique.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab2cd-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-123">Указывает тип объекта базы данных, для которого необходимо задать разрешения или владельца.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-123">Specifies the type of database object for which to set permissions or ownership.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab2cd-124"><a href="rightsenum.md">RightsEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-124"><a href="rightsenum.md">RightsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-125">Задает права и разрешения для группы или пользователя на объект.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-125">Specifies the rights or permissions for a group or user on an object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab2cd-126"><a href="ruleenum.md">RuleEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-126"><a href="ruleenum.md">RuleEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-127">Задает правило, которое следует придерживаться при удалении <strong>ключа</strong> .</span><span class="sxs-lookup"><span data-stu-id="ab2cd-127">Specifies the rule to follow when a <strong>Key</strong> is deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab2cd-128"><a href="sortorderenum.md">SortOrderEnum</a></span><span class="sxs-lookup"><span data-stu-id="ab2cd-128"><a href="sortorderenum.md">SortOrderEnum</a></span></span></p></td>
<td><p><span data-ttu-id="ab2cd-129">Определяет последовательность сортировки для индексированного столбца.</span><span class="sxs-lookup"><span data-stu-id="ab2cd-129">Specifies the sort sequence for an indexed column.</span></span></p></td>
</tr>
</tbody>
</table>

