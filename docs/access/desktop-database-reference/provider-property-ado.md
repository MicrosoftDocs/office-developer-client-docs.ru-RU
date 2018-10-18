---
<span data-ttu-id="741fd-101"><<<<<<< Название HEAD: TOCTitle свойство поставщика (ADO): свойство поставщика (ADO) === название: свойство поставщика (ADO) TOCTitle: свойство поставщика (ADO)</span><span class="sxs-lookup"><span data-stu-id="741fd-101"><<<<<<< HEAD title: Provider Property (ADO) TOCTitle: Provider Property (ADO) ======= title: Provider property (ADO) TOCTitle: Provider property (ADO)</span></span>
>>>>>>> <span data-ttu-id="741fd-102">главные ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID: 48543543 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="741fd-102">master ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID: 48543543 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="741fd-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="741fd-103"><<<<<<< HEAD</span></span>
# <a name="provider-property-ado"></a><span data-ttu-id="741fd-104">Provider Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="741fd-104">Provider Property (ADO)</span></span>
=======
# <a name="provider-property-ado"></a><span data-ttu-id="741fd-105">Свойство поставщика (ADO)</span><span class="sxs-lookup"><span data-stu-id="741fd-105">Provider property (ADO)</span></span>
>>>>>>> <span data-ttu-id="741fd-106">master</span><span class="sxs-lookup"><span data-stu-id="741fd-106">master</span></span>


<span data-ttu-id="741fd-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="741fd-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="741fd-108">Указывает имя поставщика для объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="741fd-108">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="741fd-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="741fd-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="741fd-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="741fd-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="741fd-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="741fd-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="741fd-112">master</span><span class="sxs-lookup"><span data-stu-id="741fd-112">master</span></span>

<span data-ttu-id="741fd-113">Задает или возвращает **строковое** значение, указывающее имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="741fd-113">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="741fd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="741fd-114">Remarks</span></span>

<span data-ttu-id="741fd-115">Используйте свойство **поставщика** или возвращает имя поставщика для подключения.</span><span class="sxs-lookup"><span data-stu-id="741fd-115">Use the **Provider** property to set or return the name of the provider for a connection.</span></span> <span data-ttu-id="741fd-116">Это свойство также можно установить с содержимое со значением свойства [ConnectionString](connectionstring-property-ado.md) или аргумент *ConnectionString* метода [Open](open-method-ado-connection.md) ; Тем не менее определение поставщика в нескольких местах, во время вызова метода **Open** может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="741fd-116">This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results.</span></span> <span data-ttu-id="741fd-117">Если поставщик не указан, свойство по умолчанию MSDASQL ([Поставщик Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)).</span><span class="sxs-lookup"><span data-stu-id="741fd-117">If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="741fd-118">Свойство **поставщика** — чтение и запись при подключении закрытой и только для чтения при открытии.</span><span class="sxs-lookup"><span data-stu-id="741fd-118">The **Provider** property is read/write when the connection is closed and read-only when it is open.</span></span> <span data-ttu-id="741fd-119">Параметр вступает в силу до при открытии объект **подключения** или коллекции [свойств](properties-collection-ado.md) объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="741fd-119">The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object.</span></span> <span data-ttu-id="741fd-120">Если параметр не является допустимым, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="741fd-120">If the setting is not valid, an error occurs.</span></span>

