---
title: Метод Relations.Append (DAO)
TOCTitle: Append Method
ms:assetid: dafcc7b8-b30d-2ba2-631d-eca0f882fc2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835334(v=office.15)
ms:contentKeyID: 48548094
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052904
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c3f8ee64f7eff6b02ddf4a004eaec7364436e0d1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998422"
---
# <a name="relationsappend-method-dao"></a><span data-ttu-id="48434-102">Метод Relations.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="48434-102">Relations.Append method (DAO)</span></span>

<span data-ttu-id="48434-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48434-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48434-104">Добавляет нового **отношения** в коллекции **отношений** .</span><span class="sxs-lookup"><span data-stu-id="48434-104">Adds a new **Relation** to the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="48434-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48434-105">Syntax</span></span>

<span data-ttu-id="48434-106">*выражение* . Добавление (***объект***)</span><span class="sxs-lookup"><span data-stu-id="48434-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="48434-107">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="48434-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="48434-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="48434-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48434-109">Имя</span><span class="sxs-lookup"><span data-stu-id="48434-109">Name</span></span></p></th>
<th><p><span data-ttu-id="48434-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="48434-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="48434-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="48434-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="48434-112">Описание</span><span class="sxs-lookup"><span data-stu-id="48434-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48434-113"><em>Объект</em></span><span class="sxs-lookup"><span data-stu-id="48434-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="48434-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="48434-114">Required</span></span></p></td>
<td><p><span data-ttu-id="48434-115"><strong>Объект</strong></span><span class="sxs-lookup"><span data-stu-id="48434-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="48434-116">Объектная переменная, представляющий поле, добавленный в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="48434-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="48434-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="48434-117">Remarks</span></span>

<span data-ttu-id="48434-118">Добавленный объект становится сохраняемого объекта, хранящиеся на диске, пока не будет удалена с помощью метода **Delete** .</span><span class="sxs-lookup"><span data-stu-id="48434-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="48434-119">Добавление нового объекта выполняется немедленно, но следует использовать метод **Refresh** в семействах сайтов, которые может затронуть изменения структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="48434-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="48434-120">Если объект, в которую добавляются не завершена (например, при любые объекты **поля** еще не добавлены в коллекцию **полей** **индекс** объекта до добавляется к коллекции **индексов** ) или задать свойства в одном или нескольких неправильные подчиненных объектов, с помощью метода **Append** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="48434-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="48434-121">Например если вы еще не указан тип поля и попытайтесь добавьте объект **поля** в коллекцию **полей** в объекте **TableDef** , с помощью метода **Append** запускает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="48434-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

