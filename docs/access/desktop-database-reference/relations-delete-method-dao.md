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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306967"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="be8d9-102">Метод Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="be8d9-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="be8d9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be8d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be8d9-104">Удаляет указанное **отношение из** коллекции **Relations.**</span><span class="sxs-lookup"><span data-stu-id="be8d9-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be8d9-105">Syntax</span></span>

<span data-ttu-id="be8d9-106">*выражения* . Удаление ***(Имя)***</span><span class="sxs-lookup"><span data-stu-id="be8d9-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="be8d9-107">*выражение* Переменная, представляюная объект **Relations.**</span><span class="sxs-lookup"><span data-stu-id="be8d9-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="be8d9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be8d9-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be8d9-109">Имя</span><span class="sxs-lookup"><span data-stu-id="be8d9-109">Name</span></span></p></th>
<th><p><span data-ttu-id="be8d9-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="be8d9-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="be8d9-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="be8d9-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="be8d9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="be8d9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be8d9-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="be8d9-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="be8d9-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="be8d9-114">Required</span></span></p></td>
<td><p><span data-ttu-id="be8d9-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="be8d9-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="be8d9-116">Имя связи для удаления.</span><span class="sxs-lookup"><span data-stu-id="be8d9-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="be8d9-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="be8d9-117">Remarks</span></span>

<span data-ttu-id="be8d9-118">Метод **Delete** поддерживается только в том случае, если **объект Relation** — это новый, неодобренный объект.</span><span class="sxs-lookup"><span data-stu-id="be8d9-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

