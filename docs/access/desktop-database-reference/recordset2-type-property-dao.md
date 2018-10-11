---
title: Recordset2.Type Property (DAO)
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
ms.openlocfilehash: ee9afcd5367135da2d39fe889d17d089ae6f4c25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480105"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="3607d-102">Recordset2.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="3607d-102">Recordset2.Type Property (DAO)</span></span>


<span data-ttu-id="3607d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3607d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3607d-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="3607d-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="3607d-105">Только для чтения **целое число**.</span><span class="sxs-lookup"><span data-stu-id="3607d-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3607d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3607d-106">Syntax</span></span>

<span data-ttu-id="3607d-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="3607d-107">*expression* .Type</span></span>

<span data-ttu-id="3607d-108">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3607d-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3607d-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="3607d-109">Remarks</span></span>

<span data-ttu-id="3607d-110">Для объекта **набора записей** возможные параметры и возвращаемые значения, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="3607d-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3607d-111">Constant</span><span class="sxs-lookup"><span data-stu-id="3607d-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="3607d-112">Тип набора записей</span><span class="sxs-lookup"><span data-stu-id="3607d-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3607d-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="3607d-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="3607d-114">В таблице (только для рабочих областей Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="3607d-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3607d-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="3607d-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="3607d-116">Динамические (только для рабочих областей технология ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="3607d-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="3607d-117">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3607d-117">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3607d-118">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3607d-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3607d-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="3607d-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="3607d-120">Динамический набор</span><span class="sxs-lookup"><span data-stu-id="3607d-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3607d-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="3607d-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="3607d-122">Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="3607d-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3607d-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="3607d-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="3607d-124">Только вперед</span><span class="sxs-lookup"><span data-stu-id="3607d-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

