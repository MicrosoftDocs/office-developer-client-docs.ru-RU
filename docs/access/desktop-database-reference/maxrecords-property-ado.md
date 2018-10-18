---
<span data-ttu-id="cf4de-101"><<<<<<< Название HEAD: TOCTitle свойство MaxRecords (ADO): свойство MaxRecords (ADO) === заголовок: свойство MaxRecords (ADO) TOCTitle: свойство MaxRecords (ADO)</span><span class="sxs-lookup"><span data-stu-id="cf4de-101"><<<<<<< HEAD title: MaxRecords Property (ADO) TOCTitle: MaxRecords Property (ADO) ======= title: MaxRecords property (ADO) TOCTitle: MaxRecords property (ADO)</span></span>
>>>>>>> <span data-ttu-id="cf4de-102">главные ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) ms:contentKeyID: 48544475 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="cf4de-102">master ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) ms:contentKeyID: 48544475 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="cf4de-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="cf4de-103"><<<<<<< HEAD</span></span>
# <a name="maxrecords-property-ado"></a><span data-ttu-id="cf4de-104">MaxRecords Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="cf4de-104">MaxRecords Property (ADO)</span></span>
=======
# <a name="maxrecords-property-ado"></a><span data-ttu-id="cf4de-105">Свойство MaxRecords (ADO)</span><span class="sxs-lookup"><span data-stu-id="cf4de-105">MaxRecords property (ADO)</span></span>
>>>>>>> <span data-ttu-id="cf4de-106">master</span><span class="sxs-lookup"><span data-stu-id="cf4de-106">master</span></span>


<span data-ttu-id="cf4de-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf4de-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cf4de-108">Указывает максимальное число записей для возврата [набора записей](recordset-object-ado.md) из запроса.</span><span class="sxs-lookup"><span data-stu-id="cf4de-108">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

<span data-ttu-id="cf4de-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="cf4de-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="cf4de-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cf4de-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="cf4de-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cf4de-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="cf4de-112">master</span><span class="sxs-lookup"><span data-stu-id="cf4de-112">master</span></span>

<span data-ttu-id="cf4de-113">Задает или возвращает значение типа **Long** , указывающее максимальное число возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="cf4de-113">Sets or returns a **Long** value that indicates the maximum number of records to return.</span></span> <span data-ttu-id="cf4de-114">Значение по умолчанию — 0 (без ограничений).</span><span class="sxs-lookup"><span data-stu-id="cf4de-114">Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf4de-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="cf4de-115">Remarks</span></span>

<span data-ttu-id="cf4de-116">Свойство **MaxRecords** максимальное число записей, которые поставщик возвращает из источника данных.</span><span class="sxs-lookup"><span data-stu-id="cf4de-116">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source.</span></span> <span data-ttu-id="cf4de-117">По умолчанию этого свойства равно нулю, что означает, что поставщик возвращает все запрошенные записей.</span><span class="sxs-lookup"><span data-stu-id="cf4de-117">The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="cf4de-118">Свойство **MaxRecords** при чтение и запись **набора записей** закрытой и только для чтения, при открытии.</span><span class="sxs-lookup"><span data-stu-id="cf4de-118">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

