---
title: Метод Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 462581e5b1ab3f09b697ee7f4b763a889d8119fd
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925529"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="0bbd8-102">Метод Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="0bbd8-102">Relations.Delete method (DAO)</span></span>


<span data-ttu-id="0bbd8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0bbd8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0bbd8-104">Удаляет указанное **отношение** из набора **связей** .</span><span class="sxs-lookup"><span data-stu-id="0bbd8-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bbd8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bbd8-105">Syntax</span></span>

<span data-ttu-id="0bbd8-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="0bbd8-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="0bbd8-107">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="0bbd8-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0bbd8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bbd8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bbd8-109">Имя</span><span class="sxs-lookup"><span data-stu-id="0bbd8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0bbd8-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="0bbd8-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0bbd8-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0bbd8-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0bbd8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0bbd8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bbd8-113">Имя</span><span class="sxs-lookup"><span data-stu-id="0bbd8-113">Name</span></span></p></td>
<td><p><span data-ttu-id="0bbd8-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0bbd8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0bbd8-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="0bbd8-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="0bbd8-116">Имя отношения для удаления.</span><span class="sxs-lookup"><span data-stu-id="0bbd8-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0bbd8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="0bbd8-117">Remarks</span></span>

<span data-ttu-id="0bbd8-118">Метод **Delete** поддерживается только в том случае, когда объект **связи** — это новый, unappended объект.</span><span class="sxs-lookup"><span data-stu-id="0bbd8-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

