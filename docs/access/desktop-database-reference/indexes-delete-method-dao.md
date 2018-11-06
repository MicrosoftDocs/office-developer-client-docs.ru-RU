---
title: Метод Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c725919b6509b5c802502fc8280823c407516f6
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998828"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="34fa9-102">Метод Indexes.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="34fa9-102">Indexes.Delete method (DAO)</span></span>

<span data-ttu-id="34fa9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34fa9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34fa9-104">Удаляет указанный **индекс** из набора **индексов** .</span><span class="sxs-lookup"><span data-stu-id="34fa9-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="34fa9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34fa9-105">Syntax</span></span>

<span data-ttu-id="34fa9-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="34fa9-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="34fa9-107">*выражение* Переменная, которая представляет объект **индексов** .</span><span class="sxs-lookup"><span data-stu-id="34fa9-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="34fa9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="34fa9-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34fa9-109">Имя</span><span class="sxs-lookup"><span data-stu-id="34fa9-109">Name</span></span></p></th>
<th><p><span data-ttu-id="34fa9-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="34fa9-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="34fa9-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="34fa9-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="34fa9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="34fa9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34fa9-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="34fa9-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="34fa9-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="34fa9-114">Required</span></span></p></td>
<td><p><span data-ttu-id="34fa9-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="34fa9-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="34fa9-116">Имя индекс, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="34fa9-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="34fa9-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="34fa9-117">Remarks</span></span>

<span data-ttu-id="34fa9-118">Метод **Delete** поддерживается только в том случае, когда объект **индекса** новые и еще не был добавлен к базе данных.</span><span class="sxs-lookup"><span data-stu-id="34fa9-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

