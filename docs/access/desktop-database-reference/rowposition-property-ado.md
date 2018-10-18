---
<span data-ttu-id="036fc-101"><<<<<<< Название HEAD: TOCTitle свойство RowPosition (ADO): свойство RowPosition (ADO) === название: свойство RowPosition (ADO) TOCTitle: свойство RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="036fc-101"><<<<<<< HEAD title: RowPosition Property (ADO) TOCTitle: RowPosition Property (ADO) ======= title: RowPosition property (ADO) TOCTitle: RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="036fc-102">главные ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: 48547325 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="036fc-102">master ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: 48547325 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="036fc-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="036fc-103"><<<<<<< HEAD</span></span>
# <a name="rowposition-property-ado"></a><span data-ttu-id="036fc-104">RowPosition Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="036fc-104">RowPosition Property (ADO)</span></span>
=======
# <a name="rowposition-property-ado"></a><span data-ttu-id="036fc-105">Свойство RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="036fc-105">RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="036fc-106">master</span><span class="sxs-lookup"><span data-stu-id="036fc-106">master</span></span>


<span data-ttu-id="036fc-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="036fc-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="036fc-108">Получает или задает объект OLE DB **RowPosition** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="036fc-108">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="036fc-109">При использовании **поместить\_RowPosition** Чтобы установить для объекта **RowPosition** , объекте результирующего **набора записей** использует объект **RowPosition** для определения текущей строки.</span><span class="sxs-lookup"><span data-stu-id="036fc-109">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="036fc-110">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="036fc-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="036fc-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="036fc-111">Syntax</span></span>

<span data-ttu-id="036fc-112">HRESULT get\_RowPosition (\[out retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="036fc-112">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="036fc-113">Поместите HRESULT\_RowPosition (\[в\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="036fc-113">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="036fc-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="036fc-114">Parameters</span></span>

  - <span data-ttu-id="036fc-115">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="036fc-115">*ppRowPos*</span></span>

  - <span data-ttu-id="036fc-116">Указатель на объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="036fc-116">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="036fc-117">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="036fc-117">*PRowPos*</span></span>

  - <span data-ttu-id="036fc-118">Объект OLE DB **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="036fc-118">An OLE DB **RowPosition** object.</span></span>

<span data-ttu-id="036fc-119"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="036fc-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="036fc-120">Return Values</span><span class="sxs-lookup"><span data-stu-id="036fc-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="036fc-121">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="036fc-121">Return values</span></span>
>>>>>>> <span data-ttu-id="036fc-122">master</span><span class="sxs-lookup"><span data-stu-id="036fc-122">master</span></span>

<span data-ttu-id="036fc-123">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="036fc-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="036fc-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="036fc-124">Remarks</span></span>

<span data-ttu-id="036fc-125">Если значение этого свойства, если объекта **набора записей** в объекте **RowPosition** отличается от объекта **набора записей** в объекте **набора записей** , бывшие переопределяет второй.</span><span class="sxs-lookup"><span data-stu-id="036fc-125">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="036fc-126">То же самое относится к текущей **главы** **RowPosition** также.</span><span class="sxs-lookup"><span data-stu-id="036fc-126">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="036fc-127">Применимо к</span><span class="sxs-lookup"><span data-stu-id="036fc-127">Applies To</span></span>

[<span data-ttu-id="036fc-128">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="036fc-128">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

