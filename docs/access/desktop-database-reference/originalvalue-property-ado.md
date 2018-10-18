---
<span data-ttu-id="a5475-101"><<<<<<< Название HEAD: TOCTitle свойство OriginalValue (ADO): свойство OriginalValue (ADO) === название: свойство OriginalValue (ADO) TOCTitle: свойство OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="a5475-101"><<<<<<< HEAD title: OriginalValue Property (ADO) TOCTitle: OriginalValue Property (ADO) ======= title: OriginalValue property (ADO) TOCTitle: OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a5475-102">главные ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: 48542974 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a5475-102">master ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: 48542974 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="a5475-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a5475-103"><<<<<<< HEAD</span></span>
# <a name="originalvalue-property-ado"></a><span data-ttu-id="a5475-104">OriginalValue Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="a5475-104">OriginalValue Property (ADO)</span></span>
=======
# <a name="originalvalue-property-ado"></a><span data-ttu-id="a5475-105">Свойство OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="a5475-105">OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a5475-106">master</span><span class="sxs-lookup"><span data-stu-id="a5475-106">master</span></span>

<span data-ttu-id="a5475-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5475-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a5475-108">Указывает значение [поля](field-object-ado.md) , которое существовало в записи до внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="a5475-108">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

<span data-ttu-id="a5475-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a5475-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="a5475-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5475-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="a5475-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5475-111">Return value</span></span>
>>>>>>> <span data-ttu-id="a5475-112">master</span><span class="sxs-lookup"><span data-stu-id="a5475-112">master</span></span>

<span data-ttu-id="a5475-113">Возвращает значение **типа Variant** , который представляет значение поля до изменения.</span><span class="sxs-lookup"><span data-stu-id="a5475-113">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5475-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5475-114">Remarks</span></span>

<span data-ttu-id="a5475-115">Свойство **OriginalValue** возвращает исходное значение поля для поля из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a5475-115">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="a5475-116">В *режиме немедленное обновление* (где поставщик записывает изменения к базовому источнику данных после вызова метода [обновления](update-method-ado.md) ) это свойство **OriginalValue** возвращает значение поля, существовавшего до внесения изменений (то есть, поскольку Последнее **обновление** вызова метода).</span><span class="sxs-lookup"><span data-stu-id="a5475-116">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="a5475-117">Это то же значение, метод [CancelUpdate](cancelupdate-method-ado.md) используется для замены свойства [Value](value-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a5475-117">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="a5475-118">В *пакетном режиме обновления* (в котором поставщик кэширует несколько изменений и записывает их в источнике данных только при вызове метода [UpdateBatch](updatebatch-method-ado.md) ) это свойство **OriginalValue** возвращает значение поля, существовавшего до какие-либо изменяет (то есть, с момента последнего метода **UpdateBatch** звонков).</span><span class="sxs-lookup"><span data-stu-id="a5475-118">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="a5475-119">Это то же значение, метод [CancelBatch](cancelbatch-method-ado.md) используется для замены свойства **Value** .</span><span class="sxs-lookup"><span data-stu-id="a5475-119">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="a5475-120">При использовании этого свойства с помощью свойства [UnderlyingValue](underlyingvalue-property-ado.md) можно разрешения конфликтов с помощью пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="a5475-120">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="a5475-121">Запись</span><span class="sxs-lookup"><span data-stu-id="a5475-121">Record</span></span>

<span data-ttu-id="a5475-122">Для [записи](record-object-ado.md) объектов **OriginalValue** свойство будет пустым для полей, добавлены, прежде чем будет вызван метод [Update](update-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a5475-122">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

