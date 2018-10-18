---
<span data-ttu-id="7996b-101"><<<<<<< Название HEAD: TOCTitle свойство ConnectionTimeout (ADO): свойство ConnectionTimeout (ADO) === название: свойство ConnectionTimeout (ADO) TOCTitle: свойство ConnectionTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="7996b-101"><<<<<<< HEAD title: ConnectionTimeout Property (ADO) TOCTitle: ConnectionTimeout Property (ADO) ======= title: ConnectionTimeout property (ADO) TOCTitle: ConnectionTimeout property (ADO)</span></span>
>>>>>>> <span data-ttu-id="7996b-102">главные ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15) ms:contentKeyID: 48548589 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="7996b-102">master ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15) ms:contentKeyID: 48548589 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="7996b-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="7996b-103"><<<<<<< HEAD</span></span>
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="7996b-104">ConnectionTimeout Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="7996b-104">ConnectionTimeout Property (ADO)</span></span>
=======
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="7996b-105">Свойство ConnectionTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="7996b-105">ConnectionTimeout property (ADO)</span></span>
>>>>>>> <span data-ttu-id="7996b-106">master</span><span class="sxs-lookup"><span data-stu-id="7996b-106">master</span></span>


<span data-ttu-id="7996b-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7996b-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7996b-108">Указывает время ожидания при установке соединения перед завершается и генерируется ошибка.</span><span class="sxs-lookup"><span data-stu-id="7996b-108">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

<span data-ttu-id="7996b-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="7996b-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="7996b-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7996b-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="7996b-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7996b-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="7996b-112">master</span><span class="sxs-lookup"><span data-stu-id="7996b-112">master</span></span>

<span data-ttu-id="7996b-113">Задает или возвращает значение типа **Long** , которое указывает, в секундах, время ожидания для подключения открыть.</span><span class="sxs-lookup"><span data-stu-id="7996b-113">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open.</span></span> <span data-ttu-id="7996b-114">Значение по умолчанию — 15.</span><span class="sxs-lookup"><span data-stu-id="7996b-114">Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="7996b-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="7996b-115">Remarks</span></span>

<span data-ttu-id="7996b-116">Используйте свойство **ConnectionTimeout** на объект [подключения](connection-object-ado.md) Если использовать задержки сетевого трафика или высокая интенсивность операций сервера необходимо отменить попытку подключения.</span><span class="sxs-lookup"><span data-stu-id="7996b-116">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt.</span></span> <span data-ttu-id="7996b-117">Если перед открытием подключения истечения времени от настройки свойства **ConnectionTimeout** , возникает ошибка, и ADO отменяет попытку.</span><span class="sxs-lookup"><span data-stu-id="7996b-117">If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt.</span></span> <span data-ttu-id="7996b-118">Если задать свойству присваивается значение 0, ADO будет ждать неограниченное время открытия подключения.</span><span class="sxs-lookup"><span data-stu-id="7996b-118">If you set the property to zero, ADO will wait indefinitely until the connection is opened.</span></span> <span data-ttu-id="7996b-119">Убедитесь, что поставщик, к которому написании кода поддерживает функциональную возможность **ConnectionTimeout** .</span><span class="sxs-lookup"><span data-stu-id="7996b-119">Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="7996b-120">Свойство **ConnectionTimeout** — чтение и запись в случае подключения закрытой и только для чтения при открытии.</span><span class="sxs-lookup"><span data-stu-id="7996b-120">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

