---
<span data-ttu-id="c0d4e-101"><<<<<<< Название HEAD: TOCTitle свойство главы (ADO): свойство главы (ADO) === название: свойство главы (ADO) TOCTitle: свойство главы (ADO)</span><span class="sxs-lookup"><span data-stu-id="c0d4e-101"><<<<<<< HEAD title: Chapter Property (ADO) TOCTitle: Chapter Property (ADO) ======= title: Chapter property (ADO) TOCTitle: Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c0d4e-102">главные ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: 48548014 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="c0d4e-102">master ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: 48548014 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c0d4e-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="c0d4e-103"><<<<<<< HEAD</span></span>
# <a name="chapter-property-ado"></a><span data-ttu-id="c0d4e-104">Chapter Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="c0d4e-104">Chapter Property (ADO)</span></span>
=======
# <a name="chapter-property-ado"></a><span data-ttu-id="c0d4e-105">Свойство главы (ADO)</span><span class="sxs-lookup"><span data-stu-id="c0d4e-105">Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c0d4e-106">master</span><span class="sxs-lookup"><span data-stu-id="c0d4e-106">master</span></span>


<span data-ttu-id="c0d4e-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0d4e-107">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="c0d4e-108">Получает или задает объект OLE DB **главы** из/на объекте **ADORecordsetConstruction** .</span><span class="sxs-lookup"><span data-stu-id="c0d4e-108">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="c0d4e-109">При использовании **поместить\_главы** Чтобы установить для объекта **главы** , подмножество строк превращается в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c0d4e-109">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="c0d4e-110">Это задание текущей главы из объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="c0d4e-110">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="c0d4e-111">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c0d4e-111">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d4e-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0d4e-112">Syntax</span></span>

<span data-ttu-id="c0d4e-113">HRESULT get\_главы (\[out retval\] длинные\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="c0d4e-113">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="c0d4e-114">Поместите HRESULT\_главы (\[в\] длинные lChapter);</span><span class="sxs-lookup"><span data-stu-id="c0d4e-114">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="c0d4e-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0d4e-115">Parameters</span></span>

  - <span data-ttu-id="c0d4e-116">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="c0d4e-116">*plChapter*</span></span>

  - <span data-ttu-id="c0d4e-117">Указатель на дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="c0d4e-117">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="c0d4e-118">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="c0d4e-118">*LChapter*</span></span>

  - <span data-ttu-id="c0d4e-119">Дескриптор главы.</span><span class="sxs-lookup"><span data-stu-id="c0d4e-119">Handle of a chapter.</span></span>

<span data-ttu-id="c0d4e-120"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="c0d4e-120"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="c0d4e-121">Return Values</span><span class="sxs-lookup"><span data-stu-id="c0d4e-121">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="c0d4e-122">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c0d4e-122">Return values</span></span>
>>>>>>> <span data-ttu-id="c0d4e-123">master</span><span class="sxs-lookup"><span data-stu-id="c0d4e-123">master</span></span>

<span data-ttu-id="c0d4e-124">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="c0d4e-124">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c0d4e-125">Применимо к</span><span class="sxs-lookup"><span data-stu-id="c0d4e-125">Applies To</span></span>

[<span data-ttu-id="c0d4e-126">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="c0d4e-126">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

