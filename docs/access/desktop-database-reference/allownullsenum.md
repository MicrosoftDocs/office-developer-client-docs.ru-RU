---
title: Алловнуллсенум (Справочник по базам данных Access на компьютере)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c184253551fa3f974de1840d47654af597881cb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297168"
---
# <a name="allownullsenum"></a><span data-ttu-id="4b091-102">AllowNullsEnum</span><span class="sxs-lookup"><span data-stu-id="4b091-102">AllowNullsEnum</span></span>

<span data-ttu-id="4b091-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b091-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b091-104">Указывает, индексируются ли записи со значениями NULL.</span><span class="sxs-lookup"><span data-stu-id="4b091-104">Specifies whether records with null values are indexed.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b091-105">Константа</span><span class="sxs-lookup"><span data-stu-id="4b091-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4b091-106">Значение</span><span class="sxs-lookup"><span data-stu-id="4b091-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4b091-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4b091-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b091-108"><strong>адиндекснуллсаллов</strong></span><span class="sxs-lookup"><span data-stu-id="4b091-108"><strong>adIndexNullsAllow</strong></span></span></p></td>
<td><p><span data-ttu-id="4b091-109">нуль</span><span class="sxs-lookup"><span data-stu-id="4b091-109">0</span></span></p></td>
<td><p><span data-ttu-id="4b091-110">В индексе разрешены записи с ключевыми столбцами null.</span><span class="sxs-lookup"><span data-stu-id="4b091-110">The index does allow entries in which the key columns are null.</span></span> <span data-ttu-id="4b091-111">Если в ключевом столбце введено значение null, запись вставляется в индекс.</span><span class="sxs-lookup"><span data-stu-id="4b091-111">If a null value is entered in a key column, the entry is inserted into the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b091-112"><strong>адиндекснуллсдисаллов</strong></span><span class="sxs-lookup"><span data-stu-id="4b091-112"><strong>adIndexNullsDisallow</strong></span></span></p></td>
<td><p><span data-ttu-id="4b091-113">1,1</span><span class="sxs-lookup"><span data-stu-id="4b091-113">1</span></span></p></td>
<td><p><span data-ttu-id="4b091-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4b091-114">Default.</span></span> <span data-ttu-id="4b091-115">В индексе не допускаются записи с ключевыми столбцами null.</span><span class="sxs-lookup"><span data-stu-id="4b091-115">The index does not allow entries in which the key columns are null.</span></span> <span data-ttu-id="4b091-116">Если в ключевом столбце введено значение null, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="4b091-116">If a null value is entered in a key column, an error will occur.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b091-117"><strong>адиндекснуллсигноре</strong></span><span class="sxs-lookup"><span data-stu-id="4b091-117"><strong>adIndexNullsIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="4b091-118">2</span><span class="sxs-lookup"><span data-stu-id="4b091-118">2</span></span></p></td>
<td><p><span data-ttu-id="4b091-119">Индекс не вставляет записи, содержащие ключи null.</span><span class="sxs-lookup"><span data-stu-id="4b091-119">The index does not insert entries containing null keys.</span></span> <span data-ttu-id="4b091-120">Если в ключевом столбце введено значение null, то запись игнорируется и ошибка не возникает.</span><span class="sxs-lookup"><span data-stu-id="4b091-120">If a null value is entered in a key column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b091-121"><strong>адиндекснуллсигнореани</strong></span><span class="sxs-lookup"><span data-stu-id="4b091-121"><strong>adIndexNullsIgnoreAny</strong></span></span></p></td>
<td><p><span data-ttu-id="4b091-122">4 </span><span class="sxs-lookup"><span data-stu-id="4b091-122">4</span></span></p></td>
<td><p><span data-ttu-id="4b091-123">Индекс не вставляет записи, в которых некоторый ключевой столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="4b091-123">The index does not insert entries where some key column has a null value.</span></span> <span data-ttu-id="4b091-124">Если в индексе используется ключ с несколькими столбцами, то при вводе значения NULL в некоторый столбец Эта запись игнорируется, а ошибка не возникает.</span><span class="sxs-lookup"><span data-stu-id="4b091-124">For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
</tbody>
</table>

