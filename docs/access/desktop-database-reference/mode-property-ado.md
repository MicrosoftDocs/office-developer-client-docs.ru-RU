---
<span data-ttu-id="32fb7-101"><<<<<<< Название HEAD: TOCTitle свойство Mode (ADO): свойство Mode (ADO) === название: свойство Mode (ADO) TOCTitle: свойство Mode (ADO)</span><span class="sxs-lookup"><span data-stu-id="32fb7-101"><<<<<<< HEAD title: Mode Property (ADO) TOCTitle: Mode Property (ADO) ======= title: Mode property (ADO) TOCTitle: Mode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="32fb7-102">главные ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15) ms:contentKeyID: 48545227 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="32fb7-102">master ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15) ms:contentKeyID: 48545227 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="32fb7-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="32fb7-103"><<<<<<< HEAD</span></span>
# <a name="mode-property-ado"></a><span data-ttu-id="32fb7-104">Mode Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="32fb7-104">Mode Property (ADO)</span></span>
=======
# <a name="mode-property-ado"></a><span data-ttu-id="32fb7-105">Свойство Mode (ADO)</span><span class="sxs-lookup"><span data-stu-id="32fb7-105">Mode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="32fb7-106">master</span><span class="sxs-lookup"><span data-stu-id="32fb7-106">master</span></span>


<span data-ttu-id="32fb7-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="32fb7-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="32fb7-108">Указывает, доступные права на изменение данных в объекте [подключения](connection-object-ado.md), [запись](record-object-ado.md)или [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="32fb7-108">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

<span data-ttu-id="32fb7-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="32fb7-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="32fb7-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="32fb7-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="32fb7-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="32fb7-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="32fb7-112">master</span><span class="sxs-lookup"><span data-stu-id="32fb7-112">master</span></span>

<span data-ttu-id="32fb7-113">Задает или возвращает значение [ConnectModeEnum](connectmodeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="32fb7-113">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value.</span></span> <span data-ttu-id="32fb7-114">Значение по умолчанию для **подключения к** : **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="32fb7-114">The default value for a **Connection** is **adModeUnknown**.</span></span> <span data-ttu-id="32fb7-115">Значение по умолчанию для объекта **записи** — **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="32fb7-115">The default value for a **Record** object is **adModeRead**.</span></span> <span data-ttu-id="32fb7-116">Значение по умолчанию для **потока** , связанного с базовым источником (открывается URL-адрес, как источник или **потока** **записи**по умолчанию) — **adModeRead**.</span><span class="sxs-lookup"><span data-stu-id="32fb7-116">The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**.</span></span> <span data-ttu-id="32fb7-117">Значение по умолчанию для **потока** , не связанные с базовым источником (создания экземпляра в памяти) — **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="32fb7-117">The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32fb7-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="32fb7-118">Remarks</span></span>

<span data-ttu-id="32fb7-119">Используйте свойство **режима** или возвращает разрешения доступа используется поставщик в текущее подключение.</span><span class="sxs-lookup"><span data-stu-id="32fb7-119">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection.</span></span> <span data-ttu-id="32fb7-120">Свойство **Mode** можно задать только при закрытии объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="32fb7-120">You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="32fb7-121">Для объекта **потока** Если режим доступа не указан, он наследуется из источника, используемого для открытия объект **Stream** .</span><span class="sxs-lookup"><span data-stu-id="32fb7-121">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object.</span></span> <span data-ttu-id="32fb7-122">Например если **поток** открыт из объекта **записи** , по умолчанию его открывается в том же режиме как **записи**.</span><span class="sxs-lookup"><span data-stu-id="32fb7-122">For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="32fb7-123">Это свойство соответствует чтения и записи, в то время как объект является закрытой и только для чтения, когда объект открыт.</span><span class="sxs-lookup"><span data-stu-id="32fb7-123">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="32fb7-124">**Службы удаленных данных об использовании** При использовании на объект подключения со стороны клиента, свойство **Mode** может устанавливаться только для **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="32fb7-124">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>

