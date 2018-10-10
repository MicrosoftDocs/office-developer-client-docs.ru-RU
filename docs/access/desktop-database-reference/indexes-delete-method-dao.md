---
title: Indexes.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b30748c0a1388a1175512e3b8d3fd1970795b821
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480640"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="aea8a-102">Indexes.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="aea8a-102">Indexes.Delete Method (DAO)</span></span>


<span data-ttu-id="aea8a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aea8a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aea8a-104">Удаляет указанный **индекс** из набора **индексов** .</span><span class="sxs-lookup"><span data-stu-id="aea8a-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea8a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aea8a-105">Syntax</span></span>

<span data-ttu-id="aea8a-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="aea8a-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="aea8a-107">*выражение* Переменная, которая представляет объект **индексов** .</span><span class="sxs-lookup"><span data-stu-id="aea8a-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="aea8a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aea8a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aea8a-109">Имя</span><span class="sxs-lookup"><span data-stu-id="aea8a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="aea8a-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="aea8a-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="aea8a-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="aea8a-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="aea8a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="aea8a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aea8a-113">Имя</span><span class="sxs-lookup"><span data-stu-id="aea8a-113">Name</span></span></p></td>
<td><p><span data-ttu-id="aea8a-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="aea8a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="aea8a-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="aea8a-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="aea8a-116">Имя индекс, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="aea8a-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aea8a-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="aea8a-117">Remarks</span></span>

<span data-ttu-id="aea8a-118">Метод **Delete** поддерживается только в том случае, когда объект **индекса** новые и еще не был добавлен к базе данных.</span><span class="sxs-lookup"><span data-stu-id="aea8a-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

