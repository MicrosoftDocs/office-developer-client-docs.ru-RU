---
title: Свойство Item (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290795"
---
# <a name="item-property-ado"></a><span data-ttu-id="3c73d-102">Свойство Item (ADO)</span><span class="sxs-lookup"><span data-stu-id="3c73d-102">Item property (ADO)</span></span>

<span data-ttu-id="3c73d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c73d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c73d-104">Указывает определенный элемент коллекции по имени или порядковому номеру.</span><span class="sxs-lookup"><span data-stu-id="3c73d-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c73d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c73d-105">Syntax</span></span>

<span data-ttu-id="3c73d-106">Задайте*object* = *коллекцию*объектов. Элемент (index)</span><span class="sxs-lookup"><span data-stu-id="3c73d-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="3c73d-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c73d-107">Return value</span></span>

<span data-ttu-id="3c73d-108">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="3c73d-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c73d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c73d-109">Parameters</span></span>

|<span data-ttu-id="3c73d-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="3c73d-110">Parameter</span></span>|<span data-ttu-id="3c73d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3c73d-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3c73d-112">*Индекс*</span><span class="sxs-lookup"><span data-stu-id="3c73d-112">*Index*</span></span> |<span data-ttu-id="3c73d-113">Выражение **типа Variant** , которое оценивается как имя или порядковый номер объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3c73d-113">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3c73d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c73d-114">Remarks</span></span>

<span data-ttu-id="3c73d-115">Используйте свойство **Item** , чтобы возвратить определенный объект в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3c73d-115">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="3c73d-116">Если **элемент** не может найти объект в коллекции, соответствующем аргументу *index* , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3c73d-116">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="3c73d-117">Кроме того, некоторые коллекции не поддерживают именованные объекты; для этих коллекций необходимо использовать ссылки на порядковые номера.</span><span class="sxs-lookup"><span data-stu-id="3c73d-117">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="3c73d-118">Свойство **Item** является свойством по умолчанию для всех коллекций; Таким образом, следующие синтаксические формы являются взаимозаменяемыми:</span><span class="sxs-lookup"><span data-stu-id="3c73d-118">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
