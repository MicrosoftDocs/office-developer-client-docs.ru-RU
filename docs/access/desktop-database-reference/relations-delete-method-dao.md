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
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="53984-102">Метод Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="53984-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="53984-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53984-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53984-104">Удаляет указанное отношение **из** коллекции **Relations.**</span><span class="sxs-lookup"><span data-stu-id="53984-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="53984-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53984-105">Syntax</span></span>

<span data-ttu-id="53984-106">*выражение .* ***Delete(Name)***</span><span class="sxs-lookup"><span data-stu-id="53984-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="53984-107">*выражение* Переменная, представляюная объект **Relations.**</span><span class="sxs-lookup"><span data-stu-id="53984-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="53984-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53984-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53984-109">Имя</span><span class="sxs-lookup"><span data-stu-id="53984-109">Name</span></span></p></th>
<th><p><span data-ttu-id="53984-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="53984-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="53984-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="53984-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="53984-112">Описание</span><span class="sxs-lookup"><span data-stu-id="53984-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53984-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="53984-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="53984-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="53984-114">Required</span></span></p></td>
<td><p><span data-ttu-id="53984-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="53984-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="53984-116">Имя удаляемого отношения.</span><span class="sxs-lookup"><span data-stu-id="53984-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="53984-117">Заметки</span><span class="sxs-lookup"><span data-stu-id="53984-117">Remarks</span></span>

<span data-ttu-id="53984-118">Метод **Delete** поддерживается только в том случае, если **объект Relation** является новым, неподдерженным объектом.</span><span class="sxs-lookup"><span data-stu-id="53984-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

