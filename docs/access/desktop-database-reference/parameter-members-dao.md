---
title: Parameter members (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288114"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="65be6-102">Parameter members (DAO)</span><span class="sxs-lookup"><span data-stu-id="65be6-102">Parameter members (DAO)</span></span>

<span data-ttu-id="65be6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65be6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65be6-104">Объект Parameter представляет значение, предоставленного запросу.</span><span class="sxs-lookup"><span data-stu-id="65be6-104">A Parameter object represents a value supplied to a query.</span></span> <span data-ttu-id="65be6-105">Параметр связан с объектом QueryDef, созданным из запроса параметра.</span><span class="sxs-lookup"><span data-stu-id="65be6-105">The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="65be6-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="65be6-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65be6-107">Имя</span><span class="sxs-lookup"><span data-stu-id="65be6-107">Name</span></span></p></th>
<th><p><span data-ttu-id="65be6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="65be6-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65be6-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span><span class="sxs-lookup"><span data-stu-id="65be6-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p><span data-ttu-id="65be6-110"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="65be6-110"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="65be6-111">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="65be6-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="65be6-112">Задает или возвращает значение, которое указывает, представляет ли объект <strong><a href="parameter-object-dao.md">Parameter</a></strong> входной параметр, выходной параметр или возвращаемого значения процедуры (только для рабочей области ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="65be6-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65be6-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="65be6-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="65be6-114">Возвращает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="65be6-114">Returns the name of the specified object.</span></span> <span data-ttu-id="65be6-115">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="65be6-115">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65be6-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="65be6-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="65be6-117">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="65be6-117">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="65be6-118">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="65be6-118">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65be6-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span><span class="sxs-lookup"><span data-stu-id="65be6-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="65be6-120">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="65be6-120">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="65be6-121">Для чтения и записи, <strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="65be6-121">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65be6-122"><strong><a href="parameter-value-property-dao.md">Значение</a></strong></span><span class="sxs-lookup"><span data-stu-id="65be6-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="65be6-123">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="65be6-123">Sets or returns the value of an object.</span></span> <span data-ttu-id="65be6-124">Для чтения и записи, <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="65be6-124">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

