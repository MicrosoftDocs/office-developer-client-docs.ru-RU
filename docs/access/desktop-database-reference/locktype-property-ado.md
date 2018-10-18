---
<span data-ttu-id="e24fb-101"><<<<<<< Название HEAD: TOCTitle LockType для свойства (ADO): LockType для свойства (ADO) === название: свойство LockType для (ADO) TOCTitle: свойство LockType для (ADO)</span><span class="sxs-lookup"><span data-stu-id="e24fb-101"><<<<<<< HEAD title: LockType Property (ADO) TOCTitle: LockType Property (ADO) ======= title: LockType property (ADO) TOCTitle: LockType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e24fb-102">главные ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15) ms:contentKeyID: 48543589 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="e24fb-102">master ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15) ms:contentKeyID: 48543589 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e24fb-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="e24fb-103"><<<<<<< HEAD</span></span>
# <a name="locktype-property-ado"></a><span data-ttu-id="e24fb-104">LockType Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="e24fb-104">LockType Property (ADO)</span></span>
=======
# <a name="locktype-property-ado"></a><span data-ttu-id="e24fb-105">Свойство LockType для (ADO)</span><span class="sxs-lookup"><span data-stu-id="e24fb-105">LockType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e24fb-106">master</span><span class="sxs-lookup"><span data-stu-id="e24fb-106">master</span></span>


<span data-ttu-id="e24fb-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e24fb-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e24fb-108">Указывает тип блокировки записей во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="e24fb-108">Indicates the type of locks placed on records during editing.</span></span>

<span data-ttu-id="e24fb-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="e24fb-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="e24fb-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e24fb-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="e24fb-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e24fb-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="e24fb-112">master</span><span class="sxs-lookup"><span data-stu-id="e24fb-112">master</span></span>

<span data-ttu-id="e24fb-113">Задает или возвращает значение [LockTypeEnum](locktypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="e24fb-113">Sets or returns a [LockTypeEnum](locktypeenum.md) value.</span></span> <span data-ttu-id="e24fb-114">Значение по умолчанию — **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="e24fb-114">The default value is **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e24fb-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="e24fb-115">Remarks</span></span>

<span data-ttu-id="e24fb-116">Присвойте свойству **LockType для** перед открытием [набора записей](recordset-object-ado.md) , чтобы указать, какой блокировки поставщика следует использовать при открытии его.</span><span class="sxs-lookup"><span data-stu-id="e24fb-116">Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it.</span></span> <span data-ttu-id="e24fb-117">Чтение свойства для возвращения типа блокировки используется open объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e24fb-117">Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="e24fb-118">Поставщики могут не поддерживать все типы блокировки.</span><span class="sxs-lookup"><span data-stu-id="e24fb-118">Providers may not support all lock types.</span></span> <span data-ttu-id="e24fb-119">Если поставщик не поддерживает запрошенный **LockType для** параметра, он будет заменить другой тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="e24fb-119">If a provider cannot support the requested **LockType** setting, it will substitute another type of locking.</span></span> <span data-ttu-id="e24fb-120">Чтобы определить фактический блокировки функциональные возможности, доступные в объекте **набора записей** , используйте метод [поддерживает](supports-method-ado.md) с **adUpdate** и **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="e24fb-120">To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="e24fb-121">Параметр **adLockPessimistic** не поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) имеет значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="e24fb-121">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span> <span data-ttu-id="e24fb-122">Если задано значение не поддерживается, сообщение об ошибке не приведет к; ближайший поддерживаемый **LockType для** будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="e24fb-122">If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="e24fb-123">Свойство **LockType для** чтения и записи при выполняется **записей** закрытой и только для чтения при открытии.</span><span class="sxs-lookup"><span data-stu-id="e24fb-123">The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="e24fb-124">**Службы удаленных данных об использовании** При использовании в объект набора записей со стороны клиента, свойство **LockType для** может устанавливаться только для **adLockBatchOptimistic**.</span><span class="sxs-lookup"><span data-stu-id="e24fb-124">**Remote Data Service Usage**When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**.</span></span>

