---
<span data-ttu-id="79f15-101"><<<<<<< Название HEAD: TOCTitle тип свойства (ADO): тип свойства (ADO) === название: введите свойство (ADO) TOCTitle: введите свойство (ADO)</span><span class="sxs-lookup"><span data-stu-id="79f15-101"><<<<<<< HEAD title: Type Property (ADO) TOCTitle: Type Property (ADO) ======= title: Type property (ADO) TOCTitle: Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="79f15-102">главные ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: 48543397 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="79f15-102">master ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: 48543397 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="79f15-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="79f15-103"><<<<<<< HEAD</span></span>
# <a name="type-property-ado"></a><span data-ttu-id="79f15-104">Type Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="79f15-104">Type Property (ADO)</span></span>
=======
# <a name="type-property-ado"></a><span data-ttu-id="79f15-105">Свойство Type (ADO)</span><span class="sxs-lookup"><span data-stu-id="79f15-105">Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="79f15-106">master</span><span class="sxs-lookup"><span data-stu-id="79f15-106">master</span></span>


<span data-ttu-id="79f15-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="79f15-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="79f15-108">Указывает тип действующие или тип данных [параметра](parameter-object-ado.md), [поля](field-object-ado.md)или [Свойства](property-object-ado.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="79f15-108">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

<span data-ttu-id="79f15-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="79f15-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="79f15-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="79f15-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="79f15-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="79f15-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="79f15-112">master</span><span class="sxs-lookup"><span data-stu-id="79f15-112">master</span></span>

<span data-ttu-id="79f15-113">Задает или возвращает значение [DataTypeEnum](datatypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="79f15-113">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79f15-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="79f15-114">Remarks</span></span>

<span data-ttu-id="79f15-115">Для **параметра** объектов свойство **Type** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="79f15-115">For **Parameter** objects, the **Type** property is read/write.</span></span> <span data-ttu-id="79f15-116">Для нового **поля** объектов, к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md) **Тип** — чтение и запись только после того, как указано [значение](value-property-ado.md) свойства для **поля** и поставщик данных имеет успешно добавлено новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="79f15-116">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="79f15-117">Для всех других объектов свойство **Type** — только для чтения.</span><span class="sxs-lookup"><span data-stu-id="79f15-117">For all other objects, the **Type** property is read-only.</span></span>

