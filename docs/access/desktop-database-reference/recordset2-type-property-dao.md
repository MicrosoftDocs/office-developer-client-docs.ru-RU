---
title: Свойство Recordset2.Type (DAO)
TOCTitle: Type Property
ms:assetid: 9bec543e-7f59-ea59-dc79-41d0e08b5ab6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198080(v=office.15)
ms:contentKeyID: 48546583
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052880
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ca75e1b21e017dfbbbc5028d06a4799a9afd50f3
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936597"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="53fcc-102">Свойство Recordset2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="53fcc-102">Recordset2.Type property (DAO)</span></span>


<span data-ttu-id="53fcc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53fcc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53fcc-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="53fcc-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="53fcc-105">Только для чтения **целое число**.</span><span class="sxs-lookup"><span data-stu-id="53fcc-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="53fcc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53fcc-106">Syntax</span></span>

<span data-ttu-id="53fcc-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="53fcc-107">*expression* .Type</span></span>

<span data-ttu-id="53fcc-108">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="53fcc-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="53fcc-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="53fcc-109">Remarks</span></span>

<span data-ttu-id="53fcc-110">Для объекта **набора записей** возможные параметры и возвращаемые значения, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="53fcc-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53fcc-111">Constant</span><span class="sxs-lookup"><span data-stu-id="53fcc-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="53fcc-112">Тип набора записей</span><span class="sxs-lookup"><span data-stu-id="53fcc-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53fcc-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="53fcc-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="53fcc-114">В таблице (только для рабочих областей Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="53fcc-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53fcc-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="53fcc-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="53fcc-116">Динамические (только для рабочих областей технология ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="53fcc-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="53fcc-117"><strong>Примечание</strong>: технология ODBCDirect рабочие области, не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="53fcc-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="53fcc-118">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="53fcc-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53fcc-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="53fcc-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="53fcc-120">Динамический набор</span><span class="sxs-lookup"><span data-stu-id="53fcc-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53fcc-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="53fcc-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="53fcc-122">Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="53fcc-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53fcc-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="53fcc-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="53fcc-124">Только вперед</span><span class="sxs-lookup"><span data-stu-id="53fcc-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

