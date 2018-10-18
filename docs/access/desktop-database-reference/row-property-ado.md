---
<span data-ttu-id="7e019-101">Заголовок: свойство строки - ActiveX Data Objects (ADO) <<<<<<< HEAD TOCTitle: свойство строки (ADO) === TOCTitle: строки свойство (ADO)</span><span class="sxs-lookup"><span data-stu-id="7e019-101">title: Row Property - ActiveX Data Objects (ADO) <<<<<<< HEAD TOCTitle: Row Property (ADO) ======= TOCTitle: Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="7e019-102">главные ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: 48543562 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="7e019-102">master ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: 48543562 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="7e019-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="7e019-103"><<<<<<< HEAD</span></span>
# <a name="row-property-ado"></a><span data-ttu-id="7e019-104">Row Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="7e019-104">Row Property (ADO)</span></span>
=======
# <a name="row-property-ado"></a><span data-ttu-id="7e019-105">Свойство строки (ADO)</span><span class="sxs-lookup"><span data-stu-id="7e019-105">Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="7e019-106">master</span><span class="sxs-lookup"><span data-stu-id="7e019-106">master</span></span>


<span data-ttu-id="7e019-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e019-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="7e019-108">Получает или задает объект OLE DB **строку** из/на объекте **ADORecordConstruction** .</span><span class="sxs-lookup"><span data-stu-id="7e019-108">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="7e019-109">При использовании **поместить\_строки** Чтобы установить для объекта **строки** , строка включается в объект ADO **записи** .</span><span class="sxs-lookup"><span data-stu-id="7e019-109">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="7e019-110">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7e019-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e019-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e019-111">Syntax</span></span>

<span data-ttu-id="7e019-112">HRESULT get\_строки (\[out retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="7e019-112">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="7e019-113">Поместите HRESULT\_строки (\[в\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="7e019-113">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="7e019-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e019-114">Parameters</span></span>

  - <span data-ttu-id="7e019-115">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="7e019-115">*ppRow*</span></span>

  - <span data-ttu-id="7e019-116">Указатель на объект OLE DB **строки** .</span><span class="sxs-lookup"><span data-stu-id="7e019-116">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="7e019-117">*PRow*</span><span class="sxs-lookup"><span data-stu-id="7e019-117">*PRow*</span></span>

  - <span data-ttu-id="7e019-118">Объект OLE DB **строки** .</span><span class="sxs-lookup"><span data-stu-id="7e019-118">An OLE DB **Row** object.</span></span>

<span data-ttu-id="7e019-119"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="7e019-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="7e019-120">Return Values</span><span class="sxs-lookup"><span data-stu-id="7e019-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="7e019-121">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7e019-121">Return values</span></span>
>>>>>>> <span data-ttu-id="7e019-122">master</span><span class="sxs-lookup"><span data-stu-id="7e019-122">master</span></span>

<span data-ttu-id="7e019-123">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="7e019-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7e019-124">Применимо к</span><span class="sxs-lookup"><span data-stu-id="7e019-124">Applies To</span></span>

[<span data-ttu-id="7e019-125">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="7e019-125">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

