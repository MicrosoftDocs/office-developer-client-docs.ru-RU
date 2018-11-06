---
title: Метод TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d511155f7a5fe1e6b83092e2065302bab99765b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999010"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="39b71-102">Метод TableDefs.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="39b71-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="39b71-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39b71-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39b71-104">Удаляет указанный объект **TableDef** из коллекции **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="39b71-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b71-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39b71-105">Syntax</span></span>

<span data-ttu-id="39b71-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="39b71-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="39b71-107">*выражение* Переменная, которая представляет собой объект- **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="39b71-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="39b71-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="39b71-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="39b71-109">Имя</span><span class="sxs-lookup"><span data-stu-id="39b71-109">Name</span></span></p></th>
<th><p><span data-ttu-id="39b71-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="39b71-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="39b71-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="39b71-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="39b71-112">Описание</span><span class="sxs-lookup"><span data-stu-id="39b71-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39b71-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="39b71-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="39b71-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="39b71-114">Required</span></span></p></td>
<td><p><span data-ttu-id="39b71-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="39b71-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="39b71-116">Имя TableDef для удаления.</span><span class="sxs-lookup"><span data-stu-id="39b71-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="39b71-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="39b71-117">Remarks</span></span>

<span data-ttu-id="39b71-118">Метод Delete поддерживается только в том случае, когда объект **TableDef** новые и еще не был добавлен к базе данных или свойство **с возможностью записи** **TableDef** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="39b71-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

