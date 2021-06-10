---
title: Объект DataControl (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ffe674f3aa02e5cc8b1f89375ca66b4efa623f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294521"
---
# <a name="datacontrol-object-rds"></a><span data-ttu-id="b6243-102">Объект DataControl (RDS)</span><span class="sxs-lookup"><span data-stu-id="b6243-102">DataControl object (RDS)</span></span>

<span data-ttu-id="b6243-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6243-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6243-104">Связывает набор записей запросов данных с одним или более элементами управления (например, текстовым полем, управлением сеткой или комбо-полем) для отображения данных **Recordset** на веб-странице. [](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b6243-104">Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a webpage.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6243-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6243-105">Syntax</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a><span data-ttu-id="b6243-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6243-106">Remarks</span></span>

<span data-ttu-id="b6243-107">ID класса для **RDS. Объект DataControl** — BD96C556-65A3-11D0-983A-00C04FC29E33.</span><span class="sxs-lookup"><span data-stu-id="b6243-107">The class ID for the **RDS.DataControl** object is BD96C556-65A3-11D0-983A-00C04FC29E33.</span></span>

> [!NOTE]
> <span data-ttu-id="b6243-108">Если вы получите ошибку, которая [является RDS. DataSpace](dataspace-object-rds.md) или **RDS. Объект DataControl** не загружается, убедитесь, что вы используете правильный ID класса.</span><span class="sxs-lookup"><span data-stu-id="b6243-108">If you get an error that an [RDS.DataSpace](dataspace-object-rds.md) or **RDS.DataControl** object doesn't load, make sure you are using the correct class ID.</span></span> <span data-ttu-id="b6243-109">ID класса для этих объектов изменены с версий 1.0 и 1.1.</span><span class="sxs-lookup"><span data-stu-id="b6243-109">The class IDs for these objects have changed from version 1.0 and 1.1.</span></span>

<span data-ttu-id="b6243-110">Для базового сценария необходимо задать только свойства **SQL,** **Подключение**  и **Server RDS. Объект DataControl,** который автоматически будет вызывать бизнес-объект по [умолчанию, RDSServer.DataFactory.](datafactory-object-rdsserver.md)</span><span class="sxs-lookup"><span data-stu-id="b6243-110">For a basic scenario, you need to set only the **SQL**, **Connect**, and **Server** properties of the **RDS.DataControl** object, which will automatically call the default business object, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span></span>

<span data-ttu-id="b6243-111">Все свойства в **RDS. DataControl** необязательный, так как настраиваемые бизнес-объекты могут заменить их функции.</span><span class="sxs-lookup"><span data-stu-id="b6243-111">All the properties in the **RDS.DataControl** are optional because custom business objects can replace their functionality.</span></span>

> [!NOTE]
> <span data-ttu-id="b6243-112">Если вы запрашиваете несколько результатов, возвращается только первый [набор](recordset-object-ado.md) записей.</span><span class="sxs-lookup"><span data-stu-id="b6243-112">If you query for multiple results, only the first [Recordset](recordset-object-ado.md) is returned.</span></span> <span data-ttu-id="b6243-113">Если требуется несколько наборов результатов, назначьте каждый из них своему **собственному DataControl**.</span><span class="sxs-lookup"><span data-stu-id="b6243-113">If multiple result sets are needed, assign each to its own **DataControl**.</span></span> 
> 
> <span data-ttu-id="b6243-114">Пример запроса для нескольких результатов может быть следующим: `"Select * from Authors, Select * from Topics"` .</span><span class="sxs-lookup"><span data-stu-id="b6243-114">An example of a query for multiple results could be the following: `"Select * from Authors, Select * from Topics"`.</span></span>

<span data-ttu-id="b6243-115">Добавление "DFMode=20;" в строку подключения при использовании **RDS. Объект DataControl** может повысить производительность сервера при обновлении данных.</span><span class="sxs-lookup"><span data-stu-id="b6243-115">Adding "DFMode=20;" to your connection string when using the **RDS.DataControl** object can improve your server's performance when updating data.</span></span> <span data-ttu-id="b6243-116">В этом параметре **объект RDSServer.DataFactory** на сервере использует менее ресурсоемкий режим.</span><span class="sxs-lookup"><span data-stu-id="b6243-116">With this setting, the **RDSServer.DataFactory** object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="b6243-117">Однако в этой конфигурации недоступны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="b6243-117">However, the following features are not available in this configuration:</span></span>

  - <span data-ttu-id="b6243-118">Использование параметризированных запросов.</span><span class="sxs-lookup"><span data-stu-id="b6243-118">Using parameterized queries.</span></span>

  - <span data-ttu-id="b6243-119">Получение сведений о параметрах или столбцах перед вызовом метода **Execute.**</span><span class="sxs-lookup"><span data-stu-id="b6243-119">Getting parameter or column information before calling the **Execute** method.</span></span>

  - <span data-ttu-id="b6243-120">Настройка **обновлений для transact true** **.**</span><span class="sxs-lookup"><span data-stu-id="b6243-120">Setting **Transact Updates** to **True**.</span></span>

  - <span data-ttu-id="b6243-121">Получение статуса строки.</span><span class="sxs-lookup"><span data-stu-id="b6243-121">Getting row status.</span></span>

  - <span data-ttu-id="b6243-122">Вызов [метода Resync.](resync-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b6243-122">Calling the [Resync](resync-method-ado.md) method.</span></span>

  - <span data-ttu-id="b6243-123">Обновление (явно или автоматически) с помощью свойства [Update Resync.](update-resync-property-dynamic-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b6243-123">Refreshing (explicitly or automatically) via the [Update Resync](update-resync-property-dynamic-ado.md) property.</span></span>

  - <span data-ttu-id="b6243-124">Настройка **свойств Command** или [Recordset.](recordset-sourcerecordset-properties-rds.md)</span><span class="sxs-lookup"><span data-stu-id="b6243-124">Setting **Command** or [Recordset](recordset-sourcerecordset-properties-rds.md) properties.</span></span>

  - <span data-ttu-id="b6243-125">Использование **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="b6243-125">Using **adCmdTableDirect**.</span></span>

<span data-ttu-id="b6243-126">The **RDS. Объект DataControl** выполняется в асинхронном режиме по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b6243-126">The **RDS.DataControl** object runs in asynchronous mode by default.</span></span> <span data-ttu-id="b6243-127">Если для приложения требуется синхронное выполнение, установите параметр [ExecuteOptions,](executeoptions-property-rds.md) равный **adcExecSync,** а параметр [FetchOptions](fetchoptions-property-rds.md) равен **adcFetchUpFront,** как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b6243-127">If you require synchronous execution for your application, set the [ExecuteOptions](executeoptions-property-rds.md) parameter equal to **adcExecSync** and the [FetchOptions](fetchoptions-property-rds.md) parameter equal to **adcFetchUpFront**, as shown in the following example.</span></span>

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

<span data-ttu-id="b6243-128">Используйте **один RDS. Объект DataControl,** связывающий результаты одного запроса с одним или более визуальными средствами управления.</span><span class="sxs-lookup"><span data-stu-id="b6243-128">Use one **RDS.DataControl** object to link the results of a single query to one or more visual controls.</span></span> <span data-ttu-id="b6243-129">Например, предположим, что вы кодировать запрос, запрашивающий данные клиента, такие как Имя, Место жительства, Место рождения, Возраст и Состояние клиента приоритета.</span><span class="sxs-lookup"><span data-stu-id="b6243-129">For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status.</span></span> <span data-ttu-id="b6243-130">Можно использовать один **RDS. Объект DataControl** для отображения имени, возраста и региона клиента в трех отдельных текстовых полях; Приоритет состояния клиента в чековом окне; и все данные в области управления сеткой.</span><span class="sxs-lookup"><span data-stu-id="b6243-130">You can use a single **RDS.DataControl** object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</span></span>

<span data-ttu-id="b6243-131">Используйте различные **RDS. Объекты DataControl** для привязки результатов нескольких запросов к различным визуальным средствам управления.</span><span class="sxs-lookup"><span data-stu-id="b6243-131">Use different **RDS.DataControl** objects to link the results of multiple queries to different visual controls.</span></span> <span data-ttu-id="b6243-132">Например, предположим, что для получения сведений о клиенте используется один запрос, а для получения сведений о товарах, приобретенных клиентом.</span><span class="sxs-lookup"><span data-stu-id="b6243-132">For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased.</span></span> <span data-ttu-id="b6243-133">Результаты первого запроса необходимо отображать в трех текстовых полях и одном флажке, а также результаты второго запроса в области управления сеткой.</span><span class="sxs-lookup"><span data-stu-id="b6243-133">You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control.</span></span> <span data-ttu-id="b6243-134">Если используется бизнес-объект по умолчанию **(RDSServer.DataFactory),** необходимо сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="b6243-134">If you use the default business object (**RDSServer.DataFactory**), you need to do the following:</span></span>

  - <span data-ttu-id="b6243-135">Добавьте **два RDS. Объекты DataControl** на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="b6243-135">Add two **RDS.DataControl** objects to your webpage.</span></span>

  - <span data-ttu-id="b6243-136">Напишите два запроса, **по одному SQL** для каждого свойства двух **RDS. Объекты DataControl.**</span><span class="sxs-lookup"><span data-stu-id="b6243-136">Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects.</span></span> <span data-ttu-id="b6243-137">Один **RDS. Объект DataControl** будет содержать SQL запрос с запросом сведений о клиентах; во втором будет содержаться запрос, запрашивающий список товаров, приобретенных клиентом.</span><span class="sxs-lookup"><span data-stu-id="b6243-137">One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</span></span>

  - <span data-ttu-id="b6243-138">В каждом из связанных меток ОБЪЕКТОВ элементов управления укажите значение DATAFLD, чтобы задать значения для данных, которые необходимо отобразить в каждом визуальном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="b6243-138">In each of the bound controls' OBJECT tags, specify the DATAFLD value to set the values for the data you want to display in each visual control.</span></span>

<span data-ttu-id="b6243-139">Ограничений на количество **RDS не существует. Объекты DataControl,** которые можно встраить с помощью тегов OBJECT на одной веб-странице.</span><span class="sxs-lookup"><span data-stu-id="b6243-139">There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single webpage.</span></span>

<span data-ttu-id="b6243-140">При определении **RDS. Объект DataControl** на веб-странице используйте значения  высоты и ширины nonzero, такие как 1 (чтобы избежать включения дополнительного пространства). </span><span class="sxs-lookup"><span data-stu-id="b6243-140">When you define the **RDS.DataControl** object on a webpage, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>

<span data-ttu-id="b6243-141">Компоненты клиентской службы удаленных данных уже включены в состав Internet Explorer 4.0; Поэтому не нужно включать параметр CODEBASE в **RDS. Тег объекта DataControl.**</span><span class="sxs-lookup"><span data-stu-id="b6243-141">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you don't need to include a CODEBASE parameter in your **RDS.DataControl** object tag.</span></span>

<span data-ttu-id="b6243-142">С помощью Internet Explorer 4.0 или более поздней модели можно связаться с данными с помощью html-элементов управления и ActiveX элементов управления только в том случае, если они помечены как элементы управления моделью квартиры.</span><span class="sxs-lookup"><span data-stu-id="b6243-142">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX controls only if they are marked as apartment model controls.</span></span>

<span data-ttu-id="b6243-143">**Microsoft Visual Basic пользователи** The **RDS. DataControl** используется только в веб-приложениях.</span><span class="sxs-lookup"><span data-stu-id="b6243-143">**Microsoft Visual Basic Users** The **RDS.DataControl** is used only in web-based applications.</span></span> <span data-ttu-id="b6243-144">Клиентская Visual Basic не нуждается в нем.</span><span class="sxs-lookup"><span data-stu-id="b6243-144">A Visual Basic client application has no need for it.</span></span>

