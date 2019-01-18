---
title: Метод Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703547"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="95f8e-102">Метод Indexes.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="95f8e-102">Indexes.Delete method (DAO)</span></span>

<span data-ttu-id="95f8e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95f8e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95f8e-104">Удаляет указанный **индекс** из набора **индексов** .</span><span class="sxs-lookup"><span data-stu-id="95f8e-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f8e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95f8e-105">Syntax</span></span>

<span data-ttu-id="95f8e-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="95f8e-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="95f8e-107">*выражение* Переменная, которая представляет объект **индексов** .</span><span class="sxs-lookup"><span data-stu-id="95f8e-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="95f8e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95f8e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95f8e-109">Имя</span><span class="sxs-lookup"><span data-stu-id="95f8e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="95f8e-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="95f8e-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="95f8e-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="95f8e-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="95f8e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="95f8e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95f8e-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="95f8e-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="95f8e-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="95f8e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="95f8e-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="95f8e-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="95f8e-116">Имя индекс, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="95f8e-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="95f8e-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="95f8e-117">Remarks</span></span>

<span data-ttu-id="95f8e-118">Метод **Delete** поддерживается только в том случае, когда объект **индекса** новые и еще не был добавлен к базе данных.</span><span class="sxs-lookup"><span data-stu-id="95f8e-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

