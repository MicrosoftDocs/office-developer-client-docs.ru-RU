---
title: Метод Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0b7fbf20a8732e8f4db525fd32bf4e5737b4d79
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716434"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="60406-102">Метод Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="60406-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="60406-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60406-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60406-104">Удаляет указанное **отношение** из набора **связей** .</span><span class="sxs-lookup"><span data-stu-id="60406-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="60406-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60406-105">Syntax</span></span>

<span data-ttu-id="60406-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="60406-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="60406-107">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="60406-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="60406-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="60406-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60406-109">Имя</span><span class="sxs-lookup"><span data-stu-id="60406-109">Name</span></span></p></th>
<th><p><span data-ttu-id="60406-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="60406-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="60406-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="60406-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="60406-112">Описание</span><span class="sxs-lookup"><span data-stu-id="60406-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60406-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="60406-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="60406-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="60406-114">Required</span></span></p></td>
<td><p><span data-ttu-id="60406-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="60406-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="60406-116">Имя отношения для удаления.</span><span class="sxs-lookup"><span data-stu-id="60406-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="60406-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="60406-117">Remarks</span></span>

<span data-ttu-id="60406-118">Метод **Delete** поддерживается только в том случае, когда объект **связи** — это новый, unappended объект.</span><span class="sxs-lookup"><span data-stu-id="60406-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

