---
<span data-ttu-id="e9024-101"><<<<<<< Название HEAD: TOCTitle свойство NativeError (ADO): свойство NativeError (ADO) === заголовок: свойство NativeError (ADO) TOCTitle: свойство NativeError (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9024-101"><<<<<<< HEAD title: NativeError Property (ADO) TOCTitle: NativeError Property (ADO) ======= title: NativeError property (ADO) TOCTitle: NativeError property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e9024-102">главные ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID: 48546685 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="e9024-102">master ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID: 48546685 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e9024-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="e9024-103"><<<<<<< HEAD</span></span>
# <a name="nativeerror-property-ado"></a><span data-ttu-id="e9024-104">NativeError Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9024-104">NativeError Property (ADO)</span></span>
=======
# <a name="nativeerror-property-ado"></a><span data-ttu-id="e9024-105">Свойство NativeError (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9024-105">NativeError property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e9024-106">master</span><span class="sxs-lookup"><span data-stu-id="e9024-106">master</span></span>


<span data-ttu-id="e9024-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9024-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e9024-108">Указывает код ошибки поставщика для того или иного объекта [ошибки](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e9024-108">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="e9024-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="e9024-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="e9024-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9024-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="e9024-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9024-111">Return value</span></span>
>>>>>>> <span data-ttu-id="e9024-112">master</span><span class="sxs-lookup"><span data-stu-id="e9024-112">master</span></span>

<span data-ttu-id="e9024-113">Возвращает значение типа **Long** , указывающее код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e9024-113">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9024-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e9024-114">Remarks</span></span>

<span data-ttu-id="e9024-115">Используйте свойство **NativeError** получение сведений о базе данных об ошибке для определенный объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="e9024-115">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object.</span></span> <span data-ttu-id="e9024-116">Например при использовании поставщика ODBC Microsoft для OLE DB с базой данных Microsoft SQL Server, коды собственной ошибки, которые создаются из SQL Server проходить через ODBC и поставщика ODBC свойство ADO **NativeError** .</span><span class="sxs-lookup"><span data-stu-id="e9024-116">For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

