---
<span data-ttu-id="ed662-101"><<<<<<< Название HEAD: TOCTitle свойство State (ADO): свойство State (ADO) === название: свойством (ADO) состояния TOCTitle: состояний свойство (ADO)</span><span class="sxs-lookup"><span data-stu-id="ed662-101"><<<<<<< HEAD title: State Property (ADO) TOCTitle: State Property (ADO) ======= title: State property (ADO) TOCTitle: State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ed662-102">главные ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: 48547053 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="ed662-102">master ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: 48547053 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="ed662-103">ado210.chm1231176 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="ed662-103">ado210.chm1231176 f1_categories:</span></span>
- <span data-ttu-id="ed662-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="ed662-104">Office.Version=v15</span></span>
---

<span data-ttu-id="ed662-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ed662-105"><<<<<<< HEAD</span></span>
# <a name="state-property-ado"></a><span data-ttu-id="ed662-106">State Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="ed662-106">State Property (ADO)</span></span>
=======
# <a name="state-property-ado"></a><span data-ttu-id="ed662-107">Свойство состояний (ADO)</span><span class="sxs-lookup"><span data-stu-id="ed662-107">State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ed662-108">master</span><span class="sxs-lookup"><span data-stu-id="ed662-108">master</span></span>


<span data-ttu-id="ed662-109">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed662-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ed662-110">Указывает для всех объектов, которые применяются ли состояние объекта открытой или закрытой.</span><span class="sxs-lookup"><span data-stu-id="ed662-110">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="ed662-111">Указывает, что все соответствующие объекты выполнения асинхронного метода, подключение, выполнение или получение текущего состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="ed662-111">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

<span data-ttu-id="ed662-112"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="ed662-112"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="ed662-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed662-113">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="ed662-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed662-114">Return value</span></span>
>>>>>>> <span data-ttu-id="ed662-115">master</span><span class="sxs-lookup"><span data-stu-id="ed662-115">master</span></span>

<span data-ttu-id="ed662-116">Возвращает значение типа **Long** , может быть [ObjectStateEnum](objectstateenum.md) значением.</span><span class="sxs-lookup"><span data-stu-id="ed662-116">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value.</span></span> <span data-ttu-id="ed662-117">Значение по умолчанию — **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="ed662-117">The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed662-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="ed662-118">Remarks</span></span>

<span data-ttu-id="ed662-119">Свойство **состояние** для определения текущего состояния того или иного объекта в любое время.</span><span class="sxs-lookup"><span data-stu-id="ed662-119">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="ed662-120">Свойство **состояние** объекта может содержать комбинацию значений.</span><span class="sxs-lookup"><span data-stu-id="ed662-120">The object's **State** property can have a combination of values.</span></span> <span data-ttu-id="ed662-121">Например если выполняется оператор, это свойство будет иметь значение объединенный **adStateOpen** и **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="ed662-121">For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="ed662-122">Свойство **State** доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ed662-122">The **State** property is read-only.</span></span>

