---
<span data-ttu-id="0a196-101"><<<<<<< Название HEAD: TOCTitle свойство строк (ADO): свойство строк (ADO) === название: набора свойств (ADO) TOCTitle: набора свойств (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a196-101"><<<<<<< HEAD title: Rowset Property (ADO) TOCTitle: Rowset Property (ADO) ======= title: Rowset property (ADO) TOCTitle: Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0a196-102">главные ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: 48543515 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0a196-102">master ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: 48543515 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0a196-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0a196-103"><<<<<<< HEAD</span></span>
# <a name="rowset-property-ado"></a><span data-ttu-id="0a196-104">Rowset Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a196-104">Rowset Property (ADO)</span></span>
=======
# <a name="rowset-property-ado"></a><span data-ttu-id="0a196-105">Набора свойств (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a196-105">Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0a196-106">master</span><span class="sxs-lookup"><span data-stu-id="0a196-106">master</span></span>


<span data-ttu-id="0a196-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a196-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="0a196-108">Получает или задает объект OLE DB **строк** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="0a196-108">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="0a196-109">При использовании put\_включается набор строк, набор строк, в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="0a196-109">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="0a196-110">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0a196-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a196-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a196-111">Syntax</span></span>

<span data-ttu-id="0a196-112">HRESULT get\_набор строк (\[out retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="0a196-112">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="0a196-113">Поместите HRESULT\_набор строк (\[в\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="0a196-113">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="0a196-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a196-114">Parameters</span></span>

  - <span data-ttu-id="0a196-115">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="0a196-115">*ppRowset*</span></span>

  - <span data-ttu-id="0a196-116">Указатель на объект OLE DB **строк** .</span><span class="sxs-lookup"><span data-stu-id="0a196-116">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="0a196-117">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="0a196-117">*PRowset*</span></span>

  - <span data-ttu-id="0a196-118">Объект OLE DB **строк** .</span><span class="sxs-lookup"><span data-stu-id="0a196-118">An OLE DB **Rowset** object.</span></span>

<span data-ttu-id="0a196-119"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0a196-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="0a196-120">Return Values</span><span class="sxs-lookup"><span data-stu-id="0a196-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="0a196-121">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0a196-121">Return values</span></span>
>>>>>>> <span data-ttu-id="0a196-122">master</span><span class="sxs-lookup"><span data-stu-id="0a196-122">master</span></span>

<span data-ttu-id="0a196-123">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="0a196-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0a196-124">Применимо к</span><span class="sxs-lookup"><span data-stu-id="0a196-124">Applies To</span></span>

[<span data-ttu-id="0a196-125">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="0a196-125">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

