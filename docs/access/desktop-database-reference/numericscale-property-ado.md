---
<span data-ttu-id="78aab-101"><<<<<<< Название HEAD: TOCTitle свойство NumericScale (ADO): свойство NumericScale (ADO) === название: свойство NumericScale (ADO) TOCTitle: свойство NumericScale (ADO)</span><span class="sxs-lookup"><span data-stu-id="78aab-101"><<<<<<< HEAD title: NumericScale Property (ADO) TOCTitle: NumericScale Property (ADO) ======= title: NumericScale property (ADO) TOCTitle: NumericScale property (ADO)</span></span>
>>>>>>> <span data-ttu-id="78aab-102">главные ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15) ms:contentKeyID: 48544824 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="78aab-102">master ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15) ms:contentKeyID: 48544824 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="78aab-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="78aab-103"><<<<<<< HEAD</span></span>
# <a name="numericscale-property-ado"></a><span data-ttu-id="78aab-104">NumericScale Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="78aab-104">NumericScale Property (ADO)</span></span>
=======
# <a name="numericscale-property-ado"></a><span data-ttu-id="78aab-105">Свойство NumericScale (ADO)</span><span class="sxs-lookup"><span data-stu-id="78aab-105">NumericScale property (ADO)</span></span>
>>>>>>> <span data-ttu-id="78aab-106">master</span><span class="sxs-lookup"><span data-stu-id="78aab-106">master</span></span>


<span data-ttu-id="78aab-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="78aab-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="78aab-108">Указывает масштаб числовых значений в объекте [параметра](parameter-object-ado.md) или [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="78aab-108">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="78aab-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="78aab-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="78aab-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="78aab-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="78aab-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="78aab-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="78aab-112">master</span><span class="sxs-lookup"><span data-stu-id="78aab-112">master</span></span>

<span data-ttu-id="78aab-113">Задает или возвращает **битное** значение, указывающее количество десятичных разрядов, к которым будут разрешены числовых значений.</span><span class="sxs-lookup"><span data-stu-id="78aab-113">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="78aab-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="78aab-114">Remarks</span></span>

<span data-ttu-id="78aab-115">Свойство **NumericScale** определяет количество цифр справа от десятичной запятой будет использоваться для представления значений для числовых объекта **параметра** или **поля** .</span><span class="sxs-lookup"><span data-stu-id="78aab-115">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="78aab-116">Для **параметра** объектов свойство **NumericScale** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="78aab-116">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="78aab-117">Для объекта **поля** **NumericScale** обычно доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="78aab-117">For a **Field** object, **NumericScale** is normally read-only.</span></span> <span data-ttu-id="78aab-118">Тем не менее для новых объектов **полей** , к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **NumericScale** — чтение и запись только после указано [значение](value-property-ado.md) свойства для **поля** и поставщика данных успешно добавил новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="78aab-118">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

