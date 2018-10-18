---
<span data-ttu-id="b6796-101"><<<<<<< Название HEAD: TOCTitle свойства источника данных (ADO): свойства источника данных (ADO) === название: свойства источника данных (ADO) TOCTitle: свойства источника данных (ADO)</span><span class="sxs-lookup"><span data-stu-id="b6796-101"><<<<<<< HEAD title: DataSource Property (ADO) TOCTitle: DataSource Property (ADO) ======= title: DataSource property (ADO) TOCTitle: DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b6796-102">главные ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: 48545087 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="b6796-102">master ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: 48545087 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="b6796-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b6796-103"><<<<<<< HEAD</span></span>
# <a name="datasource-property-ado"></a><span data-ttu-id="b6796-104">DataSource Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="b6796-104">DataSource Property (ADO)</span></span>
=======
# <a name="datasource-property-ado"></a><span data-ttu-id="b6796-105">Свойства источника данных (ADO)</span><span class="sxs-lookup"><span data-stu-id="b6796-105">DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b6796-106">master</span><span class="sxs-lookup"><span data-stu-id="b6796-106">master</span></span>


<span data-ttu-id="b6796-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6796-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b6796-108">Указывает объект, который содержит данные в виде объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b6796-108">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6796-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="b6796-109">Remarks</span></span>

<span data-ttu-id="b6796-110">Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных.</span><span class="sxs-lookup"><span data-stu-id="b6796-110">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="b6796-111">Среда данных поддерживает коллекций данных (источники данных), содержащий с именем объекты (*элементы данных*), которые будут представлены как объект **набора записей** *.*</span><span class="sxs-lookup"><span data-stu-id="b6796-111">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="b6796-112">Свойства **DataSource** и [DataMember](datamember-property-ado.md) должен использоваться вместе.</span><span class="sxs-lookup"><span data-stu-id="b6796-112">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="b6796-113">Объект, на который необходимо реализовать интерфейс **IDataSource** и должна содержать интерфейс **IRowset** .</span><span class="sxs-lookup"><span data-stu-id="b6796-113">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="b6796-114">**Использование**</span><span class="sxs-lookup"><span data-stu-id="b6796-114">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
