---
<span data-ttu-id="04832-101"><<<<<<< Название HEAD: TOCTitle свойство StayInSync (ADO): свойство StayInSync (ADO) === название: свойство StayInSync (ADO) TOCTitle: свойство StayInSync (ADO)</span><span class="sxs-lookup"><span data-stu-id="04832-101"><<<<<<< HEAD title: StayInSync Property (ADO) TOCTitle: StayInSync Property (ADO) ======= title: StayInSync property (ADO) TOCTitle: StayInSync property (ADO)</span></span>
>>>>>>> <span data-ttu-id="04832-102">главные ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID: 48542966 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="04832-102">master ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID: 48542966 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="04832-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="04832-103"><<<<<<< HEAD</span></span>
# <a name="stayinsync-property-ado"></a><span data-ttu-id="04832-104">StayInSync Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="04832-104">StayInSync Property (ADO)</span></span>
=======
# <a name="stayinsync-property-ado"></a><span data-ttu-id="04832-105">Свойство StayInSync (ADO)</span><span class="sxs-lookup"><span data-stu-id="04832-105">StayInSync property (ADO)</span></span>
>>>>>>> <span data-ttu-id="04832-106">master</span><span class="sxs-lookup"><span data-stu-id="04832-106">master</span></span>


<span data-ttu-id="04832-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="04832-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="04832-108">Указывает, в объект [набора записей](recordset-object-ado.md) иерархических ли ссылку на базовый дочерние записи (то есть, *главы*) изменяется при изменении позиции строки родительского.</span><span class="sxs-lookup"><span data-stu-id="04832-108">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

<span data-ttu-id="04832-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="04832-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="04832-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="04832-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="04832-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="04832-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="04832-112">master</span><span class="sxs-lookup"><span data-stu-id="04832-112">master</span></span>

<span data-ttu-id="04832-113">Задает или возвращает значение **типа Boolean** .</span><span class="sxs-lookup"><span data-stu-id="04832-113">Sets or returns a **Boolean** value.</span></span> <span data-ttu-id="04832-114">Значение по умолчанию — **True**.</span><span class="sxs-lookup"><span data-stu-id="04832-114">The default value is **True**.</span></span> <span data-ttu-id="04832-115">Если **значение True**, главы будут обновлены, если изменения объекта **набора записей** родительской строки положение; Если **значение False**, главы будет продолжать ссылаться на данные в предыдущей главе, даже если родительский объект **набора записей** изменилось положение строки.</span><span class="sxs-lookup"><span data-stu-id="04832-115">If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="04832-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="04832-116">Remarks</span></span>

<span data-ttu-id="04832-117">Это свойство применяется к иерархические наборы записей, такие как те, поддерживаемые [Службой формирования Microsoft данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)и должно быть равно на родительский **записей** перед дочерними извлекается **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="04832-117">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved.</span></span> <span data-ttu-id="04832-118">Это свойство упрощает переход иерархические наборы записей.</span><span class="sxs-lookup"><span data-stu-id="04832-118">This property simplifies navigating hierarchical recordsets.</span></span>

