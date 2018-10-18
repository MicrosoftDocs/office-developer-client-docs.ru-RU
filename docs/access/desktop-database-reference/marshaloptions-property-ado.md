---
<span data-ttu-id="cd1df-101"><<<<<<< Название HEAD: TOCTitle свойство MarshalOptions (ADO): свойство MarshalOptions (ADO) === название: свойство MarshalOptions (ADO) TOCTitle: свойство MarshalOptions (ADO)</span><span class="sxs-lookup"><span data-stu-id="cd1df-101"><<<<<<< HEAD title: MarshalOptions Property (ADO) TOCTitle: MarshalOptions Property (ADO) ======= title: MarshalOptions property (ADO) TOCTitle: MarshalOptions property (ADO)</span></span>
>>>>>>> <span data-ttu-id="cd1df-102">главные ms:assetid: dc9c4e94-0725-210d-8251-079054541142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15) ms:contentKeyID: 48548143 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="cd1df-102">master ms:assetid: dc9c4e94-0725-210d-8251-079054541142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15) ms:contentKeyID: 48548143 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="cd1df-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="cd1df-103"><<<<<<< HEAD</span></span>
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="cd1df-104">MarshalOptions Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="cd1df-104">MarshalOptions Property (ADO)</span></span>
=======
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="cd1df-105">Свойство MarshalOptions (ADO)</span><span class="sxs-lookup"><span data-stu-id="cd1df-105">MarshalOptions property (ADO)</span></span>
>>>>>>> <span data-ttu-id="cd1df-106">master</span><span class="sxs-lookup"><span data-stu-id="cd1df-106">master</span></span>


<span data-ttu-id="cd1df-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd1df-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cd1df-108">Указывает, какие записи для маршалинга на сервере.</span><span class="sxs-lookup"><span data-stu-id="cd1df-108">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cd1df-109">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cd1df-109">Settings And Return Values</span></span>

<span data-ttu-id="cd1df-110">Задает или возвращает значение [MarshalOptionsEnum](marshaloptionsenum.md) .</span><span class="sxs-lookup"><span data-stu-id="cd1df-110">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value.</span></span> <span data-ttu-id="cd1df-111">Значение по умолчанию — **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="cd1df-111">The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd1df-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="cd1df-112">Remarks</span></span>

<span data-ttu-id="cd1df-113"><<<<<<< HEAD при использовании со стороны клиента [записей](recordset-object-ado.md), записи, которые были изменены в клиенте записываются на средний уровень или веб-сервер, называемый маршалинга, процесс создания пакетов и отправка интерфейса параметры метода пределы потока или процесса.</span><span class="sxs-lookup"><span data-stu-id="cd1df-113"><<<<<<< HEAD When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or Web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="cd1df-114">Свойство **MarshalOptions** можно повысить производительность измененные удаленных данных — это упаковать для обновления в среднем уровне или в веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="cd1df-114">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or Web server.</span></span>
<span data-ttu-id="cd1df-115">=== При использовании со стороны клиента [записей](recordset-object-ado.md), записи, которые были изменены в клиенте записываются на средний уровень или веб-сервер, называемый маршалинга, процесс упаковки и отправки параметров метода интерфейса через границы, потока или процесса.</span><span class="sxs-lookup"><span data-stu-id="cd1df-115">======= When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="cd1df-116">Свойство **MarshalOptions** можно повысить производительность измененные удаленных данных — это упаковать для обновления в среднем уровне или в веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="cd1df-116">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>
>>>>>>> <span data-ttu-id="cd1df-117">master</span><span class="sxs-lookup"><span data-stu-id="cd1df-117">master</span></span>

<span data-ttu-id="cd1df-118">**Службы удаленных данных об использовании** Это свойство используется только на стороне клиента **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="cd1df-118">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

