---
<span data-ttu-id="6683c-101"><<<<<<< Название HEAD: TOCTitle свойство точности (ADO): свойство точности (ADO) === название: свойство точности (ADO) TOCTitle: свойство точности (ADO)</span><span class="sxs-lookup"><span data-stu-id="6683c-101"><<<<<<< HEAD title: Precision Property (ADO) TOCTitle: Precision Property (ADO) ======= title: Precision property (ADO) TOCTitle: Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6683c-102">главные ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: 48547685 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="6683c-102">master ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: 48547685 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6683c-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6683c-103"><<<<<<< HEAD</span></span>
# <a name="precision-property-ado"></a><span data-ttu-id="6683c-104">Precision Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="6683c-104">Precision Property (ADO)</span></span>
=======
# <a name="precision-property-ado"></a><span data-ttu-id="6683c-105">Свойство точности (ADO)</span><span class="sxs-lookup"><span data-stu-id="6683c-105">Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6683c-106">master</span><span class="sxs-lookup"><span data-stu-id="6683c-106">master</span></span>


<span data-ttu-id="6683c-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6683c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6683c-108">Указывает погрешность числовых значений в объект [параметра](parameter-object-ado.md) или для объектов числового [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6683c-108">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

<span data-ttu-id="6683c-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6683c-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="6683c-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6683c-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="6683c-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6683c-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="6683c-112">master</span><span class="sxs-lookup"><span data-stu-id="6683c-112">master</span></span>

<span data-ttu-id="6683c-113">Задает или возвращает **битное** значение, указывающее максимальное число знаков, используемых для представления значений.</span><span class="sxs-lookup"><span data-stu-id="6683c-113">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6683c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6683c-114">Remarks</span></span>

<span data-ttu-id="6683c-115">Свойство **точности** определяет максимальное число знаков, используемых для представления значений для числовых объекта **параметра** или **поля** .</span><span class="sxs-lookup"><span data-stu-id="6683c-115">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="6683c-116">Значение является чтение и запись в объект **параметра** .</span><span class="sxs-lookup"><span data-stu-id="6683c-116">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="6683c-117">Для объекта **поля** **точности** обычно доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6683c-117">For a **Field** object, **Precision** is normally read-only.</span></span> <span data-ttu-id="6683c-118">Тем не менее для новых объектов **полей** , к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **точность** — чтение и запись только после того, как указано [значение](value-property-ado.md) свойства для **поля** и имеет поставщика данных успешно добавлено новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="6683c-118">However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

