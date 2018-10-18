---
<span data-ttu-id="fda3e-101"><<<<<<< Название HEAD: TOCTitle свойство PageCount (ADO): свойство PageCount (ADO) === название: свойство PageCount (ADO) TOCTitle: свойство PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="fda3e-101"><<<<<<< HEAD title: PageCount Property (ADO) TOCTitle: PageCount Property (ADO) ======= title: PageCount property (ADO) TOCTitle: PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="fda3e-102">главные ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: 48546609 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="fda3e-102">master ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: 48546609 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="fda3e-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fda3e-103"><<<<<<< HEAD</span></span>
# <a name="pagecount-property-ado"></a><span data-ttu-id="fda3e-104">PageCount Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="fda3e-104">PageCount Property (ADO)</span></span>
=======
# <a name="pagecount-property-ado"></a><span data-ttu-id="fda3e-105">Свойство PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="fda3e-105">PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="fda3e-106">master</span><span class="sxs-lookup"><span data-stu-id="fda3e-106">master</span></span>


<span data-ttu-id="fda3e-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fda3e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fda3e-108">Показывает, сколько страниц данных содержит объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="fda3e-108">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

<span data-ttu-id="fda3e-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fda3e-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="fda3e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fda3e-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="fda3e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fda3e-111">Return value</span></span>
>>>>>>> <span data-ttu-id="fda3e-112">master</span><span class="sxs-lookup"><span data-stu-id="fda3e-112">master</span></span>

<span data-ttu-id="fda3e-113">Возвращает значение типа **Long** , показывает, сколько страниц в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="fda3e-113">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fda3e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fda3e-114">Remarks</span></span>

<span data-ttu-id="fda3e-115">Используйте свойство **PageCount** , чтобы определить, сколько страниц данных находятся в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="fda3e-115">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="fda3e-116">*Страницы* — это группы, размер которого равен значение свойства [PageSize](pagesize-property-ado.md) записей.</span><span class="sxs-lookup"><span data-stu-id="fda3e-116">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="fda3e-117">Даже в том случае, если последней странице не заполнен, так как меньше записей, чем значение **PageSize** , счетчиков на дополнительные в качестве значения **PageCount** .</span><span class="sxs-lookup"><span data-stu-id="fda3e-117">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="fda3e-118">Если объекта **набора записей** не поддерживает это свойство, значение будет равно -1, указывая, что **PageCount** неопределенной.</span><span class="sxs-lookup"><span data-stu-id="fda3e-118">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="fda3e-119">В разделе свойства **PageSize** и [AbsolutePage](absolutepage-property-ado.md) больше функциональных возможностей на страницу.</span><span class="sxs-lookup"><span data-stu-id="fda3e-119">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

