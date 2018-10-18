---
<span data-ttu-id="2f322-101"><<<<<<< Название HEAD: TOCTitle свойство IsolationLevel (ADO): свойство IsolationLevel (ADO) === название: свойство IsolationLevel (ADO) TOCTitle: свойство IsolationLevel (ADO)</span><span class="sxs-lookup"><span data-stu-id="2f322-101"><<<<<<< HEAD title: IsolationLevel Property (ADO) TOCTitle: IsolationLevel Property (ADO) ======= title: IsolationLevel property (ADO) TOCTitle: IsolationLevel property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2f322-102">главные ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) ms:contentKeyID: 48543493 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2f322-102">master ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) ms:contentKeyID: 48543493 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2f322-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2f322-103"><<<<<<< HEAD</span></span>
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="2f322-104">IsolationLevel Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="2f322-104">IsolationLevel Property (ADO)</span></span>
=======
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="2f322-105">Свойство IsolationLevel (ADO)</span><span class="sxs-lookup"><span data-stu-id="2f322-105">IsolationLevel property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2f322-106">master</span><span class="sxs-lookup"><span data-stu-id="2f322-106">master</span></span>


<span data-ttu-id="2f322-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f322-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f322-108">Указывает уровень изоляции для объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2f322-108">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="2f322-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2f322-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="2f322-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2f322-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="2f322-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2f322-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="2f322-112">master</span><span class="sxs-lookup"><span data-stu-id="2f322-112">master</span></span>

<span data-ttu-id="2f322-113">Задает или возвращает значение [IsolationLevelEnum](isolationlevelenum.md) .</span><span class="sxs-lookup"><span data-stu-id="2f322-113">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value.</span></span> <span data-ttu-id="2f322-114">Значение по умолчанию — **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="2f322-114">The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f322-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="2f322-115">Remarks</span></span>

<span data-ttu-id="2f322-116">Используйте свойство **IsolationLevel** , чтобы установить уровень изоляции объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="2f322-116">Use the **IsolationLevel** property to set the isolation level of a **Connection** object.</span></span> <span data-ttu-id="2f322-117">Параметр не вступят в силу только при следующем вызове метода [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2f322-117">The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method.</span></span> <span data-ttu-id="2f322-118">Если уровень изоляции, которые вы запрашиваете недоступен, поставщик может возвращать Далее больший уровень изоляции.</span><span class="sxs-lookup"><span data-stu-id="2f322-118">If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="2f322-119">Свойство **IsolationLevel** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="2f322-119">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="2f322-120">**Службы удаленных данных об использовании** При использовании на объект подключения со стороны клиента, свойство **IsolationLevel** можно задать только к **adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="2f322-120">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="2f322-121">Так как пользователей работе с отключенных объектов **наборов записей** в кэш со стороны клиента, может быть многопользовательской проблемы.</span><span class="sxs-lookup"><span data-stu-id="2f322-121">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues.</span></span> <span data-ttu-id="2f322-122">Например попытку обновления одной записи двух различных пользователей удаленной службы данных просто позволяет пользователю, сначала обновляет запись «win».</span><span class="sxs-lookup"><span data-stu-id="2f322-122">For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win."</span></span> <span data-ttu-id="2f322-123">Запрос на обновление второго пользователя завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2f322-123">The second user's update request will fail with an error.</span></span>

