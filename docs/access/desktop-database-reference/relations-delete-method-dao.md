---
title: Relations.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1a7ad2345e547232b79085ec5942ce5ca7d8b5c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870025"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="ed970-102">Relations.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="ed970-102">Relations.Delete Method (DAO)</span></span>


<span data-ttu-id="ed970-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed970-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed970-104">Удаляет указанное **отношение** из набора **связей** .</span><span class="sxs-lookup"><span data-stu-id="ed970-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed970-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed970-105">Syntax</span></span>

<span data-ttu-id="ed970-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="ed970-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="ed970-107">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="ed970-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ed970-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed970-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed970-109">Имя</span><span class="sxs-lookup"><span data-stu-id="ed970-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ed970-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="ed970-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ed970-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ed970-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ed970-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ed970-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed970-113">Имя</span><span class="sxs-lookup"><span data-stu-id="ed970-113">Name</span></span></p></td>
<td><p><span data-ttu-id="ed970-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ed970-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ed970-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="ed970-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ed970-116">Имя отношения для удаления.</span><span class="sxs-lookup"><span data-stu-id="ed970-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ed970-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="ed970-117">Remarks</span></span>

<span data-ttu-id="ed970-118">Метод **Delete** поддерживается только в том случае, когда объект **связи** — это новый, unappended объект.</span><span class="sxs-lookup"><span data-stu-id="ed970-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

