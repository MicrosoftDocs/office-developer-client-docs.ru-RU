---
title: Объект DataControl (RDS)
TOCTitle: DataControl Object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1735de700fe1b0e786f55f0539495656dd9db2d7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883003"
---
# <a name="datacontrol-object-rds"></a><span data-ttu-id="78514-102">Объект DataControl (RDS)</span><span class="sxs-lookup"><span data-stu-id="78514-102">DataControl Object (RDS)</span></span>

<span data-ttu-id="78514-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78514-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78514-104">Выполняет привязку запроса данных [набора записей](recordset-object-ado.md) для одного или нескольких элементов управления (например, текстовое поле, управления "Сетка" или поле со списком) для отображения **записей** данных на веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="78514-104">Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a webpage.</span></span>

## <a name="syntax"></a><span data-ttu-id="78514-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78514-105">Syntax</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a><span data-ttu-id="78514-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="78514-106">Remarks</span></span>

<span data-ttu-id="78514-107">КОД класса для **RDS. DataControl** BD96C556 65A3 - 11D 0-983A-00C04FC29E33 — это объект.</span><span class="sxs-lookup"><span data-stu-id="78514-107">The class ID for the **RDS.DataControl** object is BD96C556-65A3-11D0-983A-00C04FC29E33.</span></span>

> [!NOTE]
> <span data-ttu-id="78514-108">Если вы получаете сообщение об [RDS. Пространства данных](dataspace-object-rds.md) или **RDS. DataControl** объект не загружать, убедитесь, что вы используете с идентификатором правильный класс.</span><span class="sxs-lookup"><span data-stu-id="78514-108">If you get an error that an [RDS.DataSpace](dataspace-object-rds.md) or **RDS.DataControl** object doesn't load, make sure you are using the correct class ID.</span></span> <span data-ttu-id="78514-109">Класс идентификаторы для этих объектов были изменены с версии 1.0 и 1.1.</span><span class="sxs-lookup"><span data-stu-id="78514-109">The class IDs for these objects have changed from version 1.0 and 1.1.</span></span>

<span data-ttu-id="78514-110">Для базового сценария необходимо задать только свойства **RDS. **SQL**, **подключение**и **сервера** DataControl** объекта, которое будет автоматически вызывать бизнес-объекта по умолчанию [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="78514-110">For a basic scenario, you need to set only the **SQL**, **Connect**, and **Server** properties of the **RDS.DataControl** object, which will automatically call the default business object, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span></span>

<span data-ttu-id="78514-111">Все свойства **RDS. DataControl** являются необязательными, так как настраиваемые бизнес-объекты можно заменить их функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="78514-111">All the properties in the **RDS.DataControl** are optional because custom business objects can replace their functionality.</span></span>

> [!NOTE]
> <span data-ttu-id="78514-112">Если запрос для нескольких результатов, возвращается только первого [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="78514-112">If you query for multiple results, only the first [Recordset](recordset-object-ado.md) is returned.</span></span> <span data-ttu-id="78514-113">Если требуется несколько наборов результатов, назначьте каждому свой собственный **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="78514-113">If multiple result sets are needed, assign each to its own **DataControl**.</span></span> 
> 
> <span data-ttu-id="78514-114">Пример запроса для нескольких результатов может быть следующим: `"Select * from Authors, Select * from Topics"`.</span><span class="sxs-lookup"><span data-stu-id="78514-114">An example of a query for multiple results could be the following: `"Select * from Authors, Select * from Topics"`.</span></span>

<span data-ttu-id="78514-115">Добавление «DFMode = 20;» в строке подключения при использовании **RDS. DataControl** объекта может улучшить производительность сервера при обновлении данных.</span><span class="sxs-lookup"><span data-stu-id="78514-115">Adding "DFMode=20;" to your connection string when using the **RDS.DataControl** object can improve your server's performance when updating data.</span></span> <span data-ttu-id="78514-116">С помощью этого параметра, режим менее интенсивно использует объект **RDSServer.DataFactory** на сервере.</span><span class="sxs-lookup"><span data-stu-id="78514-116">With this setting, the **RDSServer.DataFactory** object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="78514-117">Тем не менее в этой конфигурации недоступны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="78514-117">However, the following features are not available in this configuration:</span></span>

  - <span data-ttu-id="78514-118">Использование запросов с параметрами.</span><span class="sxs-lookup"><span data-stu-id="78514-118">Using parameterized queries.</span></span>

  - <span data-ttu-id="78514-119">Получение сведений о параметра или столбца до вызова метода **Execute** .</span><span class="sxs-lookup"><span data-stu-id="78514-119">Getting parameter or column information before calling the **Execute** method.</span></span>

  - <span data-ttu-id="78514-120">Установка **обновлений Transact** **значения True**.</span><span class="sxs-lookup"><span data-stu-id="78514-120">Setting **Transact Updates** to **True**.</span></span>

  - <span data-ttu-id="78514-121">Начало строки состояния.</span><span class="sxs-lookup"><span data-stu-id="78514-121">Getting row status.</span></span>

  - <span data-ttu-id="78514-122">Вызов метода [выполнить повторную синхронизацию](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="78514-122">Calling the [Resync](resync-method-ado.md) method.</span></span>

  - <span data-ttu-id="78514-123">Обновление через свойство [Выполнить повторную синхронизацию обновления](update-resync-property-dynamic-ado.md) (явно или автоматически).</span><span class="sxs-lookup"><span data-stu-id="78514-123">Refreshing (explicitly or automatically) via the [Update Resync](update-resync-property-dynamic-ado.md) property.</span></span>

  - <span data-ttu-id="78514-124">Установка свойств **команда** или [набора записей](recordset-sourcerecordset-properties-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="78514-124">Setting **Command** or [Recordset](recordset-sourcerecordset-properties-rds.md) properties.</span></span>

  - <span data-ttu-id="78514-125">С помощью **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="78514-125">Using **adCmdTableDirect**.</span></span>

<span data-ttu-id="78514-126">**RDS. DataControl** объект выполняется в асинхронном режиме по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="78514-126">The **RDS.DataControl** object runs in asynchronous mode by default.</span></span> <span data-ttu-id="78514-127">Если требуется выполнять для вашего приложения, установите параметр [ExecuteOptions](executeoptions-property-rds.md) **adcExecSync** и параметр [FetchOptions](fetchoptions-property-rds.md) , равное **adcFetchUpFront**, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="78514-127">If you require synchronous execution for your application, set the [ExecuteOptions](executeoptions-property-rds.md) parameter equal to **adcExecSync** and the [FetchOptions](fetchoptions-property-rds.md) parameter equal to **adcFetchUpFront**, as shown in the following example.</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

<span data-ttu-id="78514-128">Используйте один **RDS. DataControl** объект, который требуется ссылка на один или несколько элементов управления visual результаты одного запроса.</span><span class="sxs-lookup"><span data-stu-id="78514-128">Use one **RDS.DataControl** object to link the results of a single query to one or more visual controls.</span></span> <span data-ttu-id="78514-129">Предположим, например, код запроса запрашивает данные клиента как имя, проживания, место рождения, срок хранения и состояние клиента приоритета.</span><span class="sxs-lookup"><span data-stu-id="78514-129">For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status.</span></span> <span data-ttu-id="78514-130">Можно использовать один **RDS. DataControl** объекта для отображения имени клиента, срок хранения и региона в трех отдельных текстовых полей; Приоритет состояние клиента в флажок; и все данные в элементе управления сетки.</span><span class="sxs-lookup"><span data-stu-id="78514-130">You can use a single **RDS.DataControl** object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</span></span>

<span data-ttu-id="78514-131">Использование разных **RDS. DataControl** объекты для связывания результаты нескольких запросов различные элементы управления visual.</span><span class="sxs-lookup"><span data-stu-id="78514-131">Use different **RDS.DataControl** objects to link the results of multiple queries to different visual controls.</span></span> <span data-ttu-id="78514-132">Например предположим, что используется один запрос для получения сведений о клиентах и второй запрос, чтобы получить информацию о рекламные материалы, которые клиент приобрести отдельно.</span><span class="sxs-lookup"><span data-stu-id="78514-132">For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased.</span></span> <span data-ttu-id="78514-133">Необходимо отобразить результаты первого запроса в три текстовых полей и один флажок и результаты второй запрос в элементе управления сетки.</span><span class="sxs-lookup"><span data-stu-id="78514-133">You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control.</span></span> <span data-ttu-id="78514-134">Если вы используете бизнес-объекта по умолчанию (**RDSServer.DataFactory**), необходимо выполнить следующее:</span><span class="sxs-lookup"><span data-stu-id="78514-134">If you use the default business object (**RDSServer.DataFactory**), you need to do the following:</span></span>

  - <span data-ttu-id="78514-135">Добавьте два **RDS. DataControl** объектов для веб-страница.</span><span class="sxs-lookup"><span data-stu-id="78514-135">Add two **RDS.DataControl** objects to your webpage.</span></span>

  - <span data-ttu-id="78514-136">Отправляет запрос записи два, один для каждого свойства **SQL** двух **RDS. DataControl** объектов.</span><span class="sxs-lookup"><span data-stu-id="78514-136">Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects.</span></span> <span data-ttu-id="78514-137">Один **RDS. DataControl** объекта будет содержать запрос SQL, запрашивает сведения о клиенте; второй будет содержать запрос, список товаров, которые клиент приобрести отдельно.</span><span class="sxs-lookup"><span data-stu-id="78514-137">One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</span></span>

  - <span data-ttu-id="78514-138">В каждой из тегов ОБЪЕКТОВ привязки элементов управления укажите значение DATAFLD для установки значений для данных, которые необходимо отобразить в каждом visual управления.</span><span class="sxs-lookup"><span data-stu-id="78514-138">In each of the bound controls' OBJECT tags, specify the DATAFLD value to set the values for the data you want to display in each visual control.</span></span>

<span data-ttu-id="78514-139">Нет никаких count ограничений на количество **RDS. DataControl** объектов, которые можно внедрить с помощью тегов ОБЪЕКТОВ на одной веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="78514-139">There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single webpage.</span></span>

<span data-ttu-id="78514-140">При определении **RDS. DataControl** на веб-страницы, используйте ненулевое значения **высоты** и **ширины** 1 (во избежание включения дополнительного места на диске).</span><span class="sxs-lookup"><span data-stu-id="78514-140">When you define the **RDS.DataControl** object on a webpage, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>

<span data-ttu-id="78514-141">Клиентские компоненты удаленной службы данных уже включены в Internet Explorer версии 4.0; Таким образом вам не нужно включить параметр базы кода в вашей **RDS. DataControl** тегом object.</span><span class="sxs-lookup"><span data-stu-id="78514-141">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you don't need to include a CODEBASE parameter in your **RDS.DataControl** object tag.</span></span>

<span data-ttu-id="78514-142">С Internet Explorer 4.0 или более поздней версии можно привязать к данным с помощью HTML-элементы управления и элементы управления ActiveX® только в том случае, если они помечены как элементы управления модели подразделения.</span><span class="sxs-lookup"><span data-stu-id="78514-142">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX® controls only if they are marked as apartment model controls.</span></span>

<span data-ttu-id="78514-143">**Пользователи Microsoft Visual Basic** **RDS. DataControl** используется только в веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="78514-143">**Microsoft Visual Basic Users** The **RDS.DataControl** is used only in web-based applications.</span></span> <span data-ttu-id="78514-144">Клиентского приложения Visual Basic имеет не требуется.</span><span class="sxs-lookup"><span data-stu-id="78514-144">A Visual Basic client application has no need for it.</span></span>

