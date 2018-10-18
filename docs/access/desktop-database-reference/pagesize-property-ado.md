---
<span data-ttu-id="f6961-101"><<<<<<< Название HEAD: TOCTitle свойство PageSize (ADO): свойство PageSize (ADO) === название: свойства PageSize (ADO) TOCTitle: свойства PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="f6961-101"><<<<<<< HEAD title: PageSize Property (ADO) TOCTitle: PageSize Property (ADO) ======= title: PageSize property (ADO) TOCTitle: PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f6961-102">главные ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: 48548079 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="f6961-102">master ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: 48548079 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f6961-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f6961-103"><<<<<<< HEAD</span></span>
# <a name="pagesize-property-ado"></a><span data-ttu-id="f6961-104">PageSize Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="f6961-104">PageSize Property (ADO)</span></span>
=======
# <a name="pagesize-property-ado"></a><span data-ttu-id="f6961-105">Свойства PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="f6961-105">PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f6961-106">master</span><span class="sxs-lookup"><span data-stu-id="f6961-106">master</span></span>


<span data-ttu-id="f6961-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6961-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f6961-108">Указывает, сколько записей составляют одну страницу в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f6961-108">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="f6961-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f6961-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="f6961-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f6961-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="f6961-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f6961-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="f6961-112">master</span><span class="sxs-lookup"><span data-stu-id="f6961-112">master</span></span>

<span data-ttu-id="f6961-113">Задает или возвращает значение типа **Long** , указывающее количество записей на странице.</span><span class="sxs-lookup"><span data-stu-id="f6961-113">Sets or returns a **Long** value that indicates how many records are on a page.</span></span> <span data-ttu-id="f6961-114">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f6961-114">The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6961-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="f6961-115">Remarks</span></span>

<span data-ttu-id="f6961-116"><<<<<<< HEAD свойство **PageSize** позволяет определить, сколько записей составляют логической страницы данных.</span><span class="sxs-lookup"><span data-stu-id="f6961-116"><<<<<<< HEAD Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="f6961-117">Создание размер страницы позволяет использовать свойство [AbsolutePage](absolutepage-property-ado.md) для перехода к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="f6961-117">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="f6961-118">Это полезно в сценариях веб-сервера, когда необходимо разрешить пользователю страницу с помощью данных, просмотр нескольких записей одновременно.</span><span class="sxs-lookup"><span data-stu-id="f6961-118">This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
<span data-ttu-id="f6961-119">=== Свойство **PageSize** для определения числа записей, входящих в состав логической страницы данных.</span><span class="sxs-lookup"><span data-stu-id="f6961-119">======= Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="f6961-120">Создание размер страницы позволяет использовать свойство [AbsolutePage](absolutepage-property-ado.md) для перехода к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="f6961-120">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="f6961-121">Это полезно в сценариях веб-сервера, когда необходимо разрешить пользователю страницу с помощью данных, просмотр нескольких записей одновременно.</span><span class="sxs-lookup"><span data-stu-id="f6961-121">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
>>>>>>> <span data-ttu-id="f6961-122">master</span><span class="sxs-lookup"><span data-stu-id="f6961-122">master</span></span>

<span data-ttu-id="f6961-123">Это свойство можно задать в любое время и его значение будет использоваться для расчета местоположение первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="f6961-123">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

