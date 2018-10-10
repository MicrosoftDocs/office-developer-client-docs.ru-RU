---
title: Item Property (ADO)
TOCTitle: Item Property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29453ac2801f606640fd6d9506a8ee1ee8625396
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480044"
---
# <a name="item-property-ado"></a><span data-ttu-id="98e36-102">Item Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="98e36-102">Item Property (ADO)</span></span>

<span data-ttu-id="98e36-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98e36-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="98e36-104">Указывает конкретный элемент из коллекции по имени или номеру порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="98e36-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e36-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98e36-105">Syntax</span></span>

<span data-ttu-id="98e36-106">Установить для*объекта* = *семейства сайтов*. Элемент (индекс)</span><span class="sxs-lookup"><span data-stu-id="98e36-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="98e36-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98e36-107">Return Value</span></span>

<span data-ttu-id="98e36-108">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="98e36-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="98e36-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="98e36-109">Parameters</span></span>

- <span data-ttu-id="98e36-110">*Индекс*</span><span class="sxs-lookup"><span data-stu-id="98e36-110">*Index*</span></span>

- <span data-ttu-id="98e36-111">Выражение **типа Variant** , которое оценивается как имя или порядковый номер объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="98e36-111">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e36-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="98e36-112">Remarks</span></span>

<span data-ttu-id="98e36-113">Используйте свойство **Item** для получения определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="98e36-113">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="98e36-114">Если **элемент** не удается найти объект в коллекции, соответствующий аргумент *Index* , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="98e36-114">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="98e36-115">Кроме того некоторые коллекции не поддерживают именованные объекты; для этих семейств сайтов необходимо использовать ссылки на порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="98e36-115">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="98e36-116">Свойство **Item** является свойством по умолчанию для всех семейств сайтов; Таким образом следующей формы синтаксиса являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="98e36-116">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
