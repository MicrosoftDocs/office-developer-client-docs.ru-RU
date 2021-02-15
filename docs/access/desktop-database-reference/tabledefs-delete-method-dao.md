---
title: Метод TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313995"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="a9717-102">Метод TableDefs.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9717-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="a9717-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9717-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9717-104">Удаляет указанный объект **TableDef** из коллекции **TableDefs.**</span><span class="sxs-lookup"><span data-stu-id="a9717-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9717-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9717-105">Syntax</span></span>

<span data-ttu-id="a9717-106">*выражение .* ***Delete(Name)***</span><span class="sxs-lookup"><span data-stu-id="a9717-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="a9717-107">*выражение* Переменная, представляюная объект **TableDefs.**</span><span class="sxs-lookup"><span data-stu-id="a9717-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9717-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9717-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9717-109">Имя</span><span class="sxs-lookup"><span data-stu-id="a9717-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a9717-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="a9717-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="a9717-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a9717-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="a9717-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a9717-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9717-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="a9717-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="a9717-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a9717-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a9717-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="a9717-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a9717-116">Имя TableDef, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="a9717-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a9717-117">Заметки</span><span class="sxs-lookup"><span data-stu-id="a9717-117">Remarks</span></span>

<span data-ttu-id="a9717-118">Метод Delete поддерживается только в том случае, если объект **TableDef** является новым и не был appended к базе данных, или если для свойства **Updatable** **tableDef** задано true **.**</span><span class="sxs-lookup"><span data-stu-id="a9717-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

