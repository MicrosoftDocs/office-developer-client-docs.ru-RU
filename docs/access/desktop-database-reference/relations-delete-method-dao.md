---
title: Метод отношениях. Delete (DAO)
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
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="6843d-102">Метод отношениях. Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="6843d-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="6843d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6843d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6843d-104">Удаляет указанное **отношение** из коллекции **связей** .</span><span class="sxs-lookup"><span data-stu-id="6843d-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6843d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6843d-105">Syntax</span></span>

<span data-ttu-id="6843d-106">*Expression* . Delete (***имя***)</span><span class="sxs-lookup"><span data-stu-id="6843d-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="6843d-107">*Expression (выражение* ) Переменная, представляющая объект **отношений** .</span><span class="sxs-lookup"><span data-stu-id="6843d-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6843d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6843d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6843d-109">Имя</span><span class="sxs-lookup"><span data-stu-id="6843d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6843d-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="6843d-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6843d-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6843d-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6843d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6843d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6843d-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="6843d-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="6843d-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6843d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6843d-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6843d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6843d-116">Имя отношения, которое требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="6843d-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6843d-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="6843d-117">Remarks</span></span>

<span data-ttu-id="6843d-118">Метод **Delete** поддерживается, только если объект **relation** является новым, неприсоединенным объектом.</span><span class="sxs-lookup"><span data-stu-id="6843d-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

