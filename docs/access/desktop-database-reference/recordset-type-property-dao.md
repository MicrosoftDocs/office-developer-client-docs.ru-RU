---
title: Свойство Recordset.Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85e518dc5d13a6e8e70c449fb35158395b7a13aa
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920727"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="fc6ea-102">Свойство Recordset.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="fc6ea-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="fc6ea-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc6ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc6ea-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="fc6ea-105">Только для чтения **целое число**.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6ea-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc6ea-106">Syntax</span></span>

<span data-ttu-id="fc6ea-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="fc6ea-107">*expression* .Type</span></span>

<span data-ttu-id="fc6ea-108">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="fc6ea-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc6ea-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="fc6ea-109">Remarks</span></span>

<span data-ttu-id="fc6ea-110">Для объекта **набора записей** возможные параметры и возвращаемые значения, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc6ea-111">Constant</span><span class="sxs-lookup"><span data-stu-id="fc6ea-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="fc6ea-112">Тип набора записей</span><span class="sxs-lookup"><span data-stu-id="fc6ea-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc6ea-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="fc6ea-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="fc6ea-114">В таблице (только для рабочих областей Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="fc6ea-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc6ea-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="fc6ea-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="fc6ea-116">Динамические (только для рабочих областей технология ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="fc6ea-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="fc6ea-117">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-117">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="fc6ea-118">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fc6ea-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc6ea-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="fc6ea-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="fc6ea-120">Динамический набор</span><span class="sxs-lookup"><span data-stu-id="fc6ea-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc6ea-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="fc6ea-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="fc6ea-122">Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="fc6ea-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc6ea-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="fc6ea-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="fc6ea-124">Только вперед</span><span class="sxs-lookup"><span data-stu-id="fc6ea-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

