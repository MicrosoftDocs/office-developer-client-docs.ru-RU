---
title: TableDefs.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc4d0c467d80c0eb78ea75f36b87e97ce3551631
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887189"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="a7730-102">TableDefs.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a7730-102">TableDefs.Delete Method (DAO)</span></span>


<span data-ttu-id="a7730-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7730-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7730-104">Удаляет указанный объект **TableDef** из коллекции **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="a7730-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7730-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7730-105">Syntax</span></span>

<span data-ttu-id="a7730-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="a7730-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="a7730-107">*выражение* Переменная, которая представляет собой объект- **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="a7730-107">*expression* A variable that represents a **TableDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a7730-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7730-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7730-109">Имя</span><span class="sxs-lookup"><span data-stu-id="a7730-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a7730-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="a7730-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a7730-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a7730-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a7730-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a7730-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7730-113">Имя</span><span class="sxs-lookup"><span data-stu-id="a7730-113">Name</span></span></p></td>
<td><p><span data-ttu-id="a7730-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a7730-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a7730-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="a7730-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a7730-116">Имя TableDef для удаления.</span><span class="sxs-lookup"><span data-stu-id="a7730-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a7730-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="a7730-117">Remarks</span></span>

<span data-ttu-id="a7730-118">Метод Delete поддерживается только в том случае, когда объект **TableDef** новые и еще не был добавлен к базе данных или свойство **с возможностью записи** **TableDef** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="a7730-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

