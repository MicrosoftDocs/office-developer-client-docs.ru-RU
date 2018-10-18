---
<span data-ttu-id="56736-101"><<<<<<< Название HEAD: TOCTitle свойство ActiveCommand (ADO): ms:assetid свойство ActiveCommand (ADO): 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 09/18/2015 mtps_version: v = Office.15</span><span class="sxs-lookup"><span data-stu-id="56736-101"><<<<<<< HEAD title: ActiveCommand Property (ADO) TOCTitle: ActiveCommand Property (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-ado"></a><span data-ttu-id="56736-102">ActiveCommand Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="56736-102">ActiveCommand Property (ADO)</span></span>

<span data-ttu-id="56736-103">=== Название: свойство ActiveCommand (ADO) TOCTitle: свойство (ADO) ms:assetid ActiveCommand: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 10/17/2018 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="56736-103">======= title: ActiveCommand property (ADO) TOCTitle: ActiveCommand property (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-ado"></a><span data-ttu-id="56736-104">Свойство ActiveCommand (ADO)</span><span class="sxs-lookup"><span data-stu-id="56736-104">ActiveCommand property (ADO)</span></span>
>>>>>>> <span data-ttu-id="56736-105">master</span><span class="sxs-lookup"><span data-stu-id="56736-105">master</span></span>

<span data-ttu-id="56736-106">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="56736-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="56736-107">Указывает объект [команды](command-object-ado.md) , которые созданы связанного объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="56736-107">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="56736-108"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="56736-108"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="56736-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56736-109">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="56736-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56736-110">Return value</span></span>
>>>>>>> <span data-ttu-id="56736-111">master</span><span class="sxs-lookup"><span data-stu-id="56736-111">master</span></span>

<span data-ttu-id="56736-112">Возвращает значение **типа Variant** , содержащее объект **команды** .</span><span class="sxs-lookup"><span data-stu-id="56736-112">Returns a **Variant** that contains a **Command** object.</span></span> <span data-ttu-id="56736-113">Значение по умолчанию — пустая ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="56736-113">Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="56736-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="56736-114">Remarks</span></span>

<span data-ttu-id="56736-115">Свойство **ActiveCommand** доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="56736-115">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="56736-116"><<<<<<< HEAD Если объект **команды** не использовался для создания текущего **набора записей**, то возвращается **значение Null,** ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="56736-116"><<<<<<< HEAD If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>
<span data-ttu-id="56736-117">=== Если объект **команды** не использовался для создания текущего **набора записей**, возвращается **значение Null,** ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="56736-117">======= If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>
>>>>>>> <span data-ttu-id="56736-118">master</span><span class="sxs-lookup"><span data-stu-id="56736-118">master</span></span>

<span data-ttu-id="56736-119">Это свойство используется для поиска связанного объекта **команды** , при ей предоставляется только объекте результирующего **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="56736-119">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

