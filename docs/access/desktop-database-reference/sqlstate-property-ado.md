---
<span data-ttu-id="2a102-101"><<<<<<< Название HEAD: TOCTitle свойство SQLState (ADO): свойство SQLState (ADO) === заголовок: свойство SQLState (ADO) TOCTitle: свойство SQLState (ADO)</span><span class="sxs-lookup"><span data-stu-id="2a102-101"><<<<<<< HEAD title: SQLState Property (ADO) TOCTitle: SQLState Property (ADO) ======= title: SQLState property (ADO) TOCTitle: SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2a102-102">главные ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: 48547806 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2a102-102">master ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: 48547806 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2a102-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2a102-103"><<<<<<< HEAD</span></span>
# <a name="sqlstate-property-ado"></a><span data-ttu-id="2a102-104">SQLState Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="2a102-104">SQLState Property (ADO)</span></span>
=======
# <a name="sqlstate-property-ado"></a><span data-ttu-id="2a102-105">Свойство SQLState (ADO)</span><span class="sxs-lookup"><span data-stu-id="2a102-105">SQLState property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2a102-106">master</span><span class="sxs-lookup"><span data-stu-id="2a102-106">master</span></span>


<span data-ttu-id="2a102-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a102-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a102-108">Указывает состояние SQL для того или иного объекта [ошибки](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2a102-108">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="2a102-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2a102-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="2a102-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a102-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="2a102-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a102-111">Return value</span></span>
>>>>>>> <span data-ttu-id="2a102-112">master</span><span class="sxs-lookup"><span data-stu-id="2a102-112">master</span></span>

<span data-ttu-id="2a102-113">Возвращает **строковое** значение пяти символов, которая стандарту ANSI SQL и указывает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2a102-113">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a102-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a102-114">Remarks</span></span>

<span data-ttu-id="2a102-115">Используйте свойство **SQLState** читать код ошибки пяти знаков, поставщик возвращает при возникновении ошибки во время обработки инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="2a102-115">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement.</span></span> <span data-ttu-id="2a102-116">Например при использовании поставщик Microsoft OLE DB для ODBC с базой данных Microsoft SQL Server, коды ошибок состояний SQL берутся из ODBC, основанные на ошибки, относящиеся к ODBC или на ошибки, которые создаются из Microsoft SQL Server, а затем сопоставляются с ODBC ошибки.</span><span class="sxs-lookup"><span data-stu-id="2a102-116">For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors.</span></span> <span data-ttu-id="2a102-117">Эти коды ошибок описаны в стандарте ANSI SQL, но может быть по-разному реализован различных источников данных.</span><span class="sxs-lookup"><span data-stu-id="2a102-117">These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

