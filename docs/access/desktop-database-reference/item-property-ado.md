---
<span data-ttu-id="0dc86-101"><<<<<<< Название HEAD: TOCTitle свойство Item (ADO): свойство Item (ADO) === название: свойство (ADO) элемента TOCTitle: свойство (ADO) элемента</span><span class="sxs-lookup"><span data-stu-id="0dc86-101"><<<<<<< HEAD title: Item Property (ADO) TOCTitle: Item Property (ADO) ======= title: Item property (ADO) TOCTitle: Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0dc86-102">главные ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: 48545767 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0dc86-102">master ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: 48545767 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0dc86-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0dc86-103"><<<<<<< HEAD</span></span>
# <a name="item-property-ado"></a><span data-ttu-id="0dc86-104">Item Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="0dc86-104">Item Property (ADO)</span></span>
=======
# <a name="item-property-ado"></a><span data-ttu-id="0dc86-105">Свойство Item (ADO)</span><span class="sxs-lookup"><span data-stu-id="0dc86-105">Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0dc86-106">master</span><span class="sxs-lookup"><span data-stu-id="0dc86-106">master</span></span>

<span data-ttu-id="0dc86-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dc86-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0dc86-108">Указывает конкретный элемент из коллекции по имени или номеру порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="0dc86-108">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc86-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dc86-109">Syntax</span></span>

<span data-ttu-id="0dc86-110">Установить для*объекта* = *семейства сайтов*. Элемент (индекс)</span><span class="sxs-lookup"><span data-stu-id="0dc86-110">Set*object* = *collection*.Item ( Index )</span></span>

<span data-ttu-id="0dc86-111"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0dc86-111"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="0dc86-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dc86-112">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="0dc86-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dc86-113">Return value</span></span>
>>>>>>> <span data-ttu-id="0dc86-114">master</span><span class="sxs-lookup"><span data-stu-id="0dc86-114">master</span></span>

<span data-ttu-id="0dc86-115">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="0dc86-115">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="0dc86-116">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dc86-116">Parameters</span></span>

- <span data-ttu-id="0dc86-117">*Индекс*</span><span class="sxs-lookup"><span data-stu-id="0dc86-117">*Index*</span></span>

- <span data-ttu-id="0dc86-118">Выражение **типа Variant** , которое оценивается как имя или порядковый номер объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="0dc86-118">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc86-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="0dc86-119">Remarks</span></span>

<span data-ttu-id="0dc86-120">Используйте свойство **Item** для получения определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0dc86-120">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="0dc86-121">Если **элемент** не удается найти объект в коллекции, соответствующий аргумент *Index* , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="0dc86-121">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="0dc86-122">Кроме того некоторые коллекции не поддерживают именованные объекты; для этих семейств сайтов необходимо использовать ссылки на порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="0dc86-122">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="0dc86-123">Свойство **Item** является свойством по умолчанию для всех семейств сайтов; Таким образом следующей формы синтаксиса являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="0dc86-123">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
