---
title: Indexes.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b863780208e6ea59e7c518bcb09cb20f38d30a6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887133"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="5bcf6-102">Indexes.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="5bcf6-102">Indexes.Delete Method (DAO)</span></span>


<span data-ttu-id="5bcf6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bcf6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5bcf6-104">Удаляет указанный **индекс** из набора **индексов** .</span><span class="sxs-lookup"><span data-stu-id="5bcf6-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bcf6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5bcf6-105">Syntax</span></span>

<span data-ttu-id="5bcf6-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="5bcf6-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="5bcf6-107">*выражение* Переменная, которая представляет объект **индексов** .</span><span class="sxs-lookup"><span data-stu-id="5bcf6-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="5bcf6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5bcf6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5bcf6-109">Имя</span><span class="sxs-lookup"><span data-stu-id="5bcf6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5bcf6-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="5bcf6-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="5bcf6-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5bcf6-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="5bcf6-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5bcf6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5bcf6-113">Имя</span><span class="sxs-lookup"><span data-stu-id="5bcf6-113">Name</span></span></p></td>
<td><p><span data-ttu-id="5bcf6-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5bcf6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="5bcf6-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="5bcf6-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="5bcf6-116">Имя индекс, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="5bcf6-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5bcf6-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bcf6-117">Remarks</span></span>

<span data-ttu-id="5bcf6-118">Метод **Delete** поддерживается только в том случае, когда объект **индекса** новые и еще не был добавлен к базе данных.</span><span class="sxs-lookup"><span data-stu-id="5bcf6-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

