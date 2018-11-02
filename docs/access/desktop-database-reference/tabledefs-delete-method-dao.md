---
title: Метод TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 122f30e5f6310bc180dd43582a6e1e05cc970d4b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926495"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="46fe7-102">Метод TableDefs.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="46fe7-102">TableDefs.Delete method (DAO)</span></span>


<span data-ttu-id="46fe7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46fe7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46fe7-104">Удаляет указанный объект **TableDef** из коллекции **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="46fe7-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="46fe7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46fe7-105">Syntax</span></span>

<span data-ttu-id="46fe7-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="46fe7-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="46fe7-107">*выражение* Переменная, которая представляет собой объект- **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="46fe7-107">*expression* A variable that represents a **TableDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="46fe7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46fe7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46fe7-109">Имя</span><span class="sxs-lookup"><span data-stu-id="46fe7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="46fe7-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="46fe7-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="46fe7-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="46fe7-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="46fe7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="46fe7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46fe7-113">Имя</span><span class="sxs-lookup"><span data-stu-id="46fe7-113">Name</span></span></p></td>
<td><p><span data-ttu-id="46fe7-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="46fe7-114">Required</span></span></p></td>
<td><p><span data-ttu-id="46fe7-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="46fe7-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="46fe7-116">Имя TableDef для удаления.</span><span class="sxs-lookup"><span data-stu-id="46fe7-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="46fe7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="46fe7-117">Remarks</span></span>

<span data-ttu-id="46fe7-118">Метод Delete поддерживается только в том случае, когда объект **TableDef** новые и еще не был добавлен к базе данных или свойство **с возможностью записи** **TableDef** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="46fe7-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

