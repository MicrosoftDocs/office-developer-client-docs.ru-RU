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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291554"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="b4c59-102">Метод Indexes.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="b4c59-102">Indexes.Delete method (DAO)</span></span>

<span data-ttu-id="b4c59-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4c59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4c59-104">Удаляет указанный **индекс** из коллекции **Indexes.**</span><span class="sxs-lookup"><span data-stu-id="b4c59-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c59-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4c59-105">Syntax</span></span>

<span data-ttu-id="b4c59-106">*выражения* . Удаление ***(Имя)***</span><span class="sxs-lookup"><span data-stu-id="b4c59-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="b4c59-107">*выражение* Переменная, представляюная объект **Indexes.**</span><span class="sxs-lookup"><span data-stu-id="b4c59-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4c59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4c59-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4c59-109">Имя</span><span class="sxs-lookup"><span data-stu-id="b4c59-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b4c59-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="b4c59-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b4c59-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b4c59-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b4c59-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b4c59-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4c59-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="b4c59-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b4c59-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b4c59-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b4c59-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="b4c59-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b4c59-116">Имя удаляемого индекса.</span><span class="sxs-lookup"><span data-stu-id="b4c59-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b4c59-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4c59-117">Remarks</span></span>

<span data-ttu-id="b4c59-118">Метод **Delete** поддерживается только в том случае, если объект **Index** является новым и не был задан в базу данных.</span><span class="sxs-lookup"><span data-stu-id="b4c59-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

