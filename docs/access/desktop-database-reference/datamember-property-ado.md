---
<span data-ttu-id="bd089-101"><<<<<<< Название HEAD: TOCTitle свойство DataMember (ADO): свойство DataMember (ADO) === название: свойства DataMember (ADO) TOCTitle: свойства DataMember (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd089-101"><<<<<<< HEAD title: DataMember Property (ADO) TOCTitle: DataMember Property (ADO) ======= title: DataMember property (ADO) TOCTitle: DataMember property (ADO)</span></span>
>>>>>>> <span data-ttu-id="bd089-102">главные ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) ms:contentKeyID: 48548787 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="bd089-102">master ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) ms:contentKeyID: 48548787 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="bd089-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="bd089-103"><<<<<<< HEAD</span></span>
# <a name="datamember-property-ado"></a><span data-ttu-id="bd089-104">DataMember Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd089-104">DataMember Property (ADO)</span></span>
=======
# <a name="datamember-property-ado"></a><span data-ttu-id="bd089-105">Свойство DataMember (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd089-105">DataMember property (ADO)</span></span>
>>>>>>> <span data-ttu-id="bd089-106">master</span><span class="sxs-lookup"><span data-stu-id="bd089-106">master</span></span>

<span data-ttu-id="bd089-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd089-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bd089-108">Указывает имя элемента данных, который извлекается из объекта ссылается свойство [DataSource](datasource-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bd089-108">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

<span data-ttu-id="bd089-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="bd089-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="bd089-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bd089-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="bd089-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bd089-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="bd089-112">master</span><span class="sxs-lookup"><span data-stu-id="bd089-112">master</span></span>

<span data-ttu-id="bd089-113">Задает или возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="bd089-113">Sets or returns a **String** value.</span></span> <span data-ttu-id="bd089-114">Имя не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="bd089-114">The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd089-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd089-115">Remarks</span></span>

<span data-ttu-id="bd089-116">Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных.</span><span class="sxs-lookup"><span data-stu-id="bd089-116">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="bd089-117">Среда данных поддерживает коллекций данных (источники данных), содержащий с именем объекты (*элементы данных*), которые будут представлены как объект [набора записей](recordset-object-ado.md) *.*</span><span class="sxs-lookup"><span data-stu-id="bd089-117">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="bd089-118">Свойства **DataSource** и **DataMember** должен использоваться вместе.</span><span class="sxs-lookup"><span data-stu-id="bd089-118">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="bd089-119">Свойство **DataMember** определяет, какие объекта, заданного в свойстве **DataSource** будут представлены как объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="bd089-119">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object.</span></span> <span data-ttu-id="bd089-120">Объект **набора записей** должны быть закрыты, это свойство задано.</span><span class="sxs-lookup"><span data-stu-id="bd089-120">The **Recordset** object must be closed before this property is set.</span></span> <span data-ttu-id="bd089-121">Ошибка создается в том случае, если свойство **DataMember** не будет установлено перед свойства **источника данных** или имя **DataMember** не распознается объектом, указанных в свойстве **DataSource** .</span><span class="sxs-lookup"><span data-stu-id="bd089-121">An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="bd089-122">**Использование**</span><span class="sxs-lookup"><span data-stu-id="bd089-122">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
