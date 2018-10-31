---
<span data-ttu-id="f0559-101"><<<<<<< Название HEAD: TOCTitle свойство EditMode (ADO): свойство EditMode (ADO) === название: свойство EditMode (ADO) TOCTitle: свойство EditMode (ADO)</span><span class="sxs-lookup"><span data-stu-id="f0559-101"><<<<<<< HEAD title: EditMode Property (ADO) TOCTitle: EditMode Property (ADO) ======= title: EditMode property (ADO) TOCTitle: EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f0559-102">главные ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: 48543867 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="f0559-102">master ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: 48543867 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f0559-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f0559-103"><<<<<<< HEAD</span></span>
# <a name="editmode-property-ado"></a><span data-ttu-id="f0559-104">Свойство EditMode (ADO)</span><span class="sxs-lookup"><span data-stu-id="f0559-104">EditMode Property (ADO)</span></span>
=======
# <a name="editmode-property-ado"></a><span data-ttu-id="f0559-105">Свойство EditMode (ADO)</span><span class="sxs-lookup"><span data-stu-id="f0559-105">EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f0559-106">образец</span><span class="sxs-lookup"><span data-stu-id="f0559-106">master</span></span>


<span data-ttu-id="f0559-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0559-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f0559-108">Указывает состояние редактирования текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f0559-108">Indicates the editing status of the current record.</span></span>

<span data-ttu-id="f0559-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f0559-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="f0559-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0559-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="f0559-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0559-111">Return value</span></span>
>>>>>>> <span data-ttu-id="f0559-112">образец</span><span class="sxs-lookup"><span data-stu-id="f0559-112">master</span></span>

<span data-ttu-id="f0559-113">Возвращает значение [EditModeEnum](editmodeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="f0559-113">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0559-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f0559-114">Remarks</span></span>

<span data-ttu-id="f0559-115">ADO поддерживает редактирования буфера, связанного с текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f0559-115">ADO maintains an editing buffer associated with the current record.</span></span> <span data-ttu-id="f0559-116">Это свойство показывает ли изменения были внесены в этот буфер или создан ли новую запись.</span><span class="sxs-lookup"><span data-stu-id="f0559-116">This property indicates whether changes have been made to this buffer, or whether a new record has been created.</span></span> <span data-ttu-id="f0559-117">Свойство **EditMode** используется для определения статуса редактирования текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f0559-117">Use the **EditMode** property to determine the editing status of the current record.</span></span> <span data-ttu-id="f0559-118">Можно проверить наличие ожидающих изменений, если редактирования процесс был прерван и определите, нужно ли использовать [обновления](update-method-ado.md) или метод [CancelUpdate](cancelupdate-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f0559-118">You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="f0559-119">В разделе метод [AddNew](addnew-method-ado.md) более подробное описание свойства **EditMode** в различных условиях редактирования.</span><span class="sxs-lookup"><span data-stu-id="f0559-119">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="f0559-120">Когда звонка для [удаления](delete-method-ado-recordset.md) успешно не удалять записи или записей в данных источника (из-за нарушения ссылочной целостности, например), [записей](recordset-object-ado.md) останется в режиме редактирования (**EditMode** = \*\*adEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="f0559-120">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="f0559-121">Это означает, что **CancelUpdate** необходимо вызывать перед перемещением off текущей записи (с [перемещением](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)и [Закрыть](close-method-ado.md), например).</span><span class="sxs-lookup"><span data-stu-id="f0559-121">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <span data-ttu-id="f0559-122">**EditMode** можно вернуть допустимое значение только в том случае, если текущая запись.</span><span class="sxs-lookup"><span data-stu-id="f0559-122">**EditMode** can return a valid value only if there is a current record.</span></span> <span data-ttu-id="f0559-123">**EditMode** возвращает ошибку, если [BOF или EOF](bof-eof-properties-ado.md) имеет значение true, или если текущий запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="f0559-123">**EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.</span></span>


