---
title: Параметр члены (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 94d3bb48da8d16a2a9cae1ec0f692a3475c57c31
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919208"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="1544b-102">Параметр члены (DAO)</span><span class="sxs-lookup"><span data-stu-id="1544b-102">Parameter members (DAO)</span></span>


<span data-ttu-id="1544b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1544b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1544b-104">Объект параметра представляет значение, заданное в запросе.</span><span class="sxs-lookup"><span data-stu-id="1544b-104">A Parameter object represents a value supplied to a query.</span></span> <span data-ttu-id="1544b-105">Параметр связан с объектом QueryDef, созданный из параметра запроса.</span><span class="sxs-lookup"><span data-stu-id="1544b-105">The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="1544b-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="1544b-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1544b-107">Имя</span><span class="sxs-lookup"><span data-stu-id="1544b-107">Name</span></span></p></th>
<th><p><span data-ttu-id="1544b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1544b-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1544b-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span><span class="sxs-lookup"><span data-stu-id="1544b-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="1544b-110">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="1544b-110">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="1544b-111">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1544b-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="1544b-112">Задает или возвращает значение, указывающее, представляет ли объект <strong><a href="parameter-object-dao.md">параметра</a></strong> входного параметра, выходного параметра, оба адресата, или возвращаемое значение из процедуры (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="1544b-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1544b-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="1544b-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1544b-114">Возвращает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="1544b-114">Returns the name of the specified object.</span></span> <span data-ttu-id="1544b-115">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="1544b-115">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1544b-116"><strong><a href="parameter-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="1544b-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1544b-117">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="1544b-117">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="1544b-118">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1544b-118">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1544b-119"><strong><a href="parameter-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="1544b-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1544b-120">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="1544b-120">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="1544b-121">Чтение и запись <strong>целое число</strong>.</span><span class="sxs-lookup"><span data-stu-id="1544b-121">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1544b-122"><strong><a href="parameter-value-property-dao.md">Значение</a></strong></span><span class="sxs-lookup"><span data-stu-id="1544b-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1544b-123">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="1544b-123">Sets or returns the value of an object.</span></span> <span data-ttu-id="1544b-124">Чтение и запись <strong>типа Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="1544b-124">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

