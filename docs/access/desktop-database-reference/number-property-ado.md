---
<span data-ttu-id="e9781-101"><<<<<<< Заголовок HEAD: TOCTitle свойство номер (ADO): свойство номер (ADO) === заголовка: число свойств (ADO) TOCTitle: номер свойство (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9781-101"><<<<<<< HEAD title: Number Property (ADO) TOCTitle: Number Property (ADO) ======= title: Number property (ADO) TOCTitle: Number property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e9781-102">главные ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15) ms:contentKeyID: 48547243 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="e9781-102">master ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15) ms:contentKeyID: 48547243 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e9781-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="e9781-103"><<<<<<< HEAD</span></span>
# <a name="number-property-ado"></a><span data-ttu-id="e9781-104">Number Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9781-104">Number Property (ADO)</span></span>
=======
# <a name="number-property-ado"></a><span data-ttu-id="e9781-105">Свойство Number (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9781-105">Number property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e9781-106">master</span><span class="sxs-lookup"><span data-stu-id="e9781-106">master</span></span>


<span data-ttu-id="e9781-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9781-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e9781-108">Указывает число, уникально идентифицирующий объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e9781-108">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="e9781-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="e9781-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="e9781-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9781-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="e9781-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9781-111">Return value</span></span>
>>>>>>> <span data-ttu-id="e9781-112">master</span><span class="sxs-lookup"><span data-stu-id="e9781-112">master</span></span>

<span data-ttu-id="e9781-113">Возвращает значение типа **Long** , могут соответствовать одному из константы [ErrorValueEnum](errorvalueenum.md) .</span><span class="sxs-lookup"><span data-stu-id="e9781-113">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9781-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e9781-114">Remarks</span></span>

<span data-ttu-id="e9781-115">Используйте свойство **номер** для определения, какая ошибка произошла.</span><span class="sxs-lookup"><span data-stu-id="e9781-115">Use the **Number** property to determine which error occurred.</span></span> <span data-ttu-id="e9781-116">Значение свойства — это уникальное число, соответствующее условия ошибки.</span><span class="sxs-lookup"><span data-stu-id="e9781-116">The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="e9781-117">Семейство [Errors](errors-collection-ado.md) возвращает значение HRESULT в шестнадцатеричном формате (например, 0x80004005) или длинное значение (например, 2147467259).</span><span class="sxs-lookup"><span data-stu-id="e9781-117">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="e9781-118">Эти значения HRESULT может вызываться базовых компонентах, таких как OLE DB или даже OLE самого.</span><span class="sxs-lookup"><span data-stu-id="e9781-118">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="e9781-119">Дополнительные сведения об этих номеров см из *Справочник программиста OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="e9781-119">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

