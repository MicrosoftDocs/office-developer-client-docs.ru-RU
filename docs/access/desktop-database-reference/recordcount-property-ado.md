---
<span data-ttu-id="796db-101"><<<<<<< Заголовок HEAD: TOCTitle свойство RecordCount (ADO): свойство RecordCount (ADO) === заголовка: свойство RecordCount (ADO) TOCTitle: свойство RecordCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="796db-101"><<<<<<< HEAD title: RecordCount Property (ADO) TOCTitle: RecordCount Property (ADO) ======= title: RecordCount property (ADO) TOCTitle: RecordCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="796db-102">главные ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15) ms:contentKeyID: 48548304 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="796db-102">master ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15) ms:contentKeyID: 48548304 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="796db-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="796db-103"><<<<<<< HEAD</span></span>
# <a name="recordcount-property-ado"></a><span data-ttu-id="796db-104">RecordCount Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="796db-104">RecordCount Property (ADO)</span></span>
=======
# <a name="recordcount-property-ado"></a><span data-ttu-id="796db-105">Свойство RecordCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="796db-105">RecordCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="796db-106">master</span><span class="sxs-lookup"><span data-stu-id="796db-106">master</span></span>


<span data-ttu-id="796db-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="796db-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="796db-108">Указывает число записей в объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="796db-108">Indicates the number of records in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="796db-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="796db-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="796db-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="796db-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="796db-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="796db-111">Return value</span></span>
>>>>>>> <span data-ttu-id="796db-112">master</span><span class="sxs-lookup"><span data-stu-id="796db-112">master</span></span>

<span data-ttu-id="796db-113">Возвращает значение типа **Long** , показывает, сколько записей в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="796db-113">Returns a **Long** value that indicates the number of records in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="796db-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="796db-114">Remarks</span></span>

<span data-ttu-id="796db-115">Используйте свойство **RecordCount** , чтобы узнать, сколько записей, в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="796db-115">Use the **RecordCount** property to find out how many records are in a **Recordset** object.</span></span> <span data-ttu-id="796db-116">Это свойство возвращает значение -1 при ADO не может определить число записей, или если поставщик или тип курсора не поддерживает **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="796db-116">The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**.</span></span> <span data-ttu-id="796db-117">Чтение свойства **RecordCount** на закрытой **набора записей** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="796db-117">Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="796db-118">Если объект **набора записей** поддерживает приблизительно, например расположение или закладки, то есть, **поддерживает (adApproxPosition)** или **поддерживает (adBookmark)**, соответственно, возвращает **значение True,** — это значение будет точное количество записей в \*\* Набор записей\*\*, независимо от того, является ли он полностью заполнен.</span><span class="sxs-lookup"><span data-stu-id="796db-118">If the **Recordset** object supports approximate positioning or bookmarks — that is, **Supports (adApproxPosition)** or **Supports (adBookmark)**, respectively, return **True** — this value will be the exact number of records in the **Recordset**, regardless of whether it has been fully populated.</span></span> <span data-ttu-id="796db-119">Если объект **набора записей** не поддерживает размещение приблизительно, например, это свойство возможно значительные затрат на ресурсы для всех записей необходимо получить и подсчитаны для возврата точное значение **RecordCount** .</span><span class="sxs-lookup"><span data-stu-id="796db-119">If the **Recordset** object does not support approximate positioning, this property may be a significant drain on resources because all records will have to be retrieved and counted to return an accurate **RecordCount** value.</span></span>

<span data-ttu-id="796db-120">Тип текущей позиции объекта **набора записей** влияет можно определить число записей.</span><span class="sxs-lookup"><span data-stu-id="796db-120">The cursor type of the **Recordset** object affects whether the number of records can be determined.</span></span> <span data-ttu-id="796db-121">Свойство **RecordCount** возвращает значение -1 для курсора последовательного доступа; Фактическое количество для static или набора ключей курсора; и значение -1 или фактический количество для динамического курсора, в зависимости от источника данных.</span><span class="sxs-lookup"><span data-stu-id="796db-121">The **RecordCount** property will return -1 for a forward-only cursor; the actual count for a static or keyset cursor; and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

