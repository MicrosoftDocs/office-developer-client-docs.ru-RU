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
# <a name="datacontrol-object-rds"></a><span data-ttu-id="3ab8c-102">Объект DataControl (RDS)</span><span class="sxs-lookup"><span data-stu-id="3ab8c-102">DataControl object (RDS)</span></span>

<span data-ttu-id="3ab8c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ab8c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ab8c-104">Привязывает набор [](recordset-object-ado.md) записей запроса данных к одному или несколько элементов управления (например, текстовом поле, элементу управления сеткой или поле со combo) для отображения данных **recordset** на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-104">Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a webpage.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ab8c-105">Syntax</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a><span data-ttu-id="3ab8c-106">Заметки</span><span class="sxs-lookup"><span data-stu-id="3ab8c-106">Remarks</span></span>

<span data-ttu-id="3ab8c-107">ИД класса для **RDS. Объект DataControl—** BD96C556-65A3-11D0-983A-00C04FC29E33.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-107">The class ID for the **RDS.DataControl** object is BD96C556-65A3-11D0-983A-00C04FC29E33.</span></span>

> [!NOTE]
> <span data-ttu-id="3ab8c-108">При ошибке [RDS. DataSpace](dataspace-object-rds.md) или **RDS. Объект DataControl** не загружается, убедитесь, что используется правильный ИД класса.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-108">If you get an error that an [RDS.DataSpace](dataspace-object-rds.md) or **RDS.DataControl** object doesn't load, make sure you are using the correct class ID.</span></span> <span data-ttu-id="3ab8c-109">ИД класса для этих объектов изменились с версий 1.0 и 1.1.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-109">The class IDs for these objects have changed from version 1.0 and 1.1.</span></span>

<span data-ttu-id="3ab8c-110">В базовом сценарии необходимо установить только свойства **SQL,** **Connect** и **Server** **RDS. Объект DataControl,** который автоматически будет вызывать бизнес-объект по умолчанию [RDSServer.DataFactory.](datafactory-object-rdsserver.md)</span><span class="sxs-lookup"><span data-stu-id="3ab8c-110">For a basic scenario, you need to set only the **SQL**, **Connect**, and **Server** properties of the **RDS.DataControl** object, which will automatically call the default business object, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span></span>

<span data-ttu-id="3ab8c-111">Все свойства в **RDS. DataControl необязательный,** так как настраиваемые бизнес-объекты могут заменить их функции.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-111">All the properties in the **RDS.DataControl** are optional because custom business objects can replace their functionality.</span></span>

> [!NOTE]
> <span data-ttu-id="3ab8c-112">При запросе нескольких результатов возвращается только [первый](recordset-object-ado.md) набор записей.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-112">If you query for multiple results, only the first [Recordset](recordset-object-ado.md) is returned.</span></span> <span data-ttu-id="3ab8c-113">Если требуется несколько наборов результатов, назначьте каждому из них собственный **DataControl.**</span><span class="sxs-lookup"><span data-stu-id="3ab8c-113">If multiple result sets are needed, assign each to its own **DataControl**.</span></span> 
> 
> <span data-ttu-id="3ab8c-114">Пример запроса для нескольких результатов может быть следующим: `"Select * from Authors, Select * from Topics"` .</span><span class="sxs-lookup"><span data-stu-id="3ab8c-114">An example of a query for multiple results could be the following: `"Select * from Authors, Select * from Topics"`.</span></span>

<span data-ttu-id="3ab8c-115">Добавление "DFMode=20;" в строку подключения при использовании **RDS. Объект DataControl** может повысить производительность сервера при обновлении данных.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-115">Adding "DFMode=20;" to your connection string when using the **RDS.DataControl** object can improve your server's performance when updating data.</span></span> <span data-ttu-id="3ab8c-116">С помощью этого параметра объект **RDSServer.DataFactory** на сервере использует менее ресурсоемкий режим.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-116">With this setting, the **RDSServer.DataFactory** object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="3ab8c-117">Однако в этой конфигурации недоступны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="3ab8c-117">However, the following features are not available in this configuration:</span></span>

  - <span data-ttu-id="3ab8c-118">Использование параметровизированных запросов.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-118">Using parameterized queries.</span></span>

  - <span data-ttu-id="3ab8c-119">Получение сведений о параметре или столбце перед вызовом **метода Execute.**</span><span class="sxs-lookup"><span data-stu-id="3ab8c-119">Getting parameter or column information before calling the **Execute** method.</span></span>

  - <span data-ttu-id="3ab8c-120">Установка **для transact-обновлений** **true.**</span><span class="sxs-lookup"><span data-stu-id="3ab8c-120">Setting **Transact Updates** to **True**.</span></span>

  - <span data-ttu-id="3ab8c-121">Получение состояния строки.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-121">Getting row status.</span></span>

  - <span data-ttu-id="3ab8c-122">Вызов метода [Resync.](resync-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3ab8c-122">Calling the [Resync](resync-method-ado.md) method.</span></span>

  - <span data-ttu-id="3ab8c-123">Обновление (явно или автоматически) с помощью свойства [Update Resync.](update-resync-property-dynamic-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3ab8c-123">Refreshing (explicitly or automatically) via the [Update Resync](update-resync-property-dynamic-ado.md) property.</span></span>

  - <span data-ttu-id="3ab8c-124">Установка **свойств Command** или [Recordset.](recordset-sourcerecordset-properties-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3ab8c-124">Setting **Command** or [Recordset](recordset-sourcerecordset-properties-rds.md) properties.</span></span>

  - <span data-ttu-id="3ab8c-125">Использование **adCmdTableDirect.**</span><span class="sxs-lookup"><span data-stu-id="3ab8c-125">Using **adCmdTableDirect**.</span></span>

<span data-ttu-id="3ab8c-126">The **RDS. Объект DataControl** выполняется в асинхронном режиме по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-126">The **RDS.DataControl** object runs in asynchronous mode by default.</span></span> <span data-ttu-id="3ab8c-127">Если для приложения требуется синхронное выполнение, установите параметр [ExecuteOptions](executeoptions-property-rds.md) равным **adcExecSync,** а параметр [FetchOptions](fetchoptions-property-rds.md) — **adcFetchUpFront,** как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-127">If you require synchronous execution for your application, set the [ExecuteOptions](executeoptions-property-rds.md) parameter equal to **adcExecSync** and the [FetchOptions](fetchoptions-property-rds.md) parameter equal to **adcFetchUpFront**, as shown in the following example.</span></span>

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

<span data-ttu-id="3ab8c-128">Используйте одну **RDS. Объект DataControl** для связывания результатов одного запроса с одним или более визуальными элементами управления.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-128">Use one **RDS.DataControl** object to link the results of a single query to one or more visual controls.</span></span> <span data-ttu-id="3ab8c-129">Например, предположим, что вы код запросили данные клиента, такие как "Имя", "Место проживания", "Место рождения", "Возраст" и "Состояние клиента с приоритетом".</span><span class="sxs-lookup"><span data-stu-id="3ab8c-129">For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status.</span></span> <span data-ttu-id="3ab8c-130">Можно использовать одну **RDS. Объект DataControl** для отображения имени, возраста и региона клиента в трех отдельных текстовых полях; Приоритет состояния клиента в окне; и все данные в сетке.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-130">You can use a single **RDS.DataControl** object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</span></span>

<span data-ttu-id="3ab8c-131">Используйте разные **RDS. Объекты DataControl** для привязки результатов нескольких запросов к различным визуальным элементы управления.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-131">Use different **RDS.DataControl** objects to link the results of multiple queries to different visual controls.</span></span> <span data-ttu-id="3ab8c-132">Например, предположим, что вы используете один запрос для получения сведений о клиенте, а второй запрос для получения сведений о товарах, приобретенных клиентом.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-132">For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased.</span></span> <span data-ttu-id="3ab8c-133">Результаты первого запроса должны отображаться в трех текстовых полях и одном флажке, а также в результатах второго запроса в сетке.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-133">You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control.</span></span> <span data-ttu-id="3ab8c-134">При использовании бизнес-объекта по умолчанию (**RDSServer.DataFactory)** необходимо сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="3ab8c-134">If you use the default business object (**RDSServer.DataFactory**), you need to do the following:</span></span>

  - <span data-ttu-id="3ab8c-135">Добавьте два **RDS. Объекты DataControl** для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-135">Add two **RDS.DataControl** objects to your webpage.</span></span>

  - <span data-ttu-id="3ab8c-136">Напишите два запроса, **по одному SQL** каждого свойства двух **RDS. Объекты DataControl.**</span><span class="sxs-lookup"><span data-stu-id="3ab8c-136">Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects.</span></span> <span data-ttu-id="3ab8c-137">Один **RDS. Объект DataControl** будет содержать SQL запроса сведений о клиенте; Вторая содержит запрос, запрашивающий список товаров, приобретенных клиентом.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-137">One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</span></span>

  - <span data-ttu-id="3ab8c-138">В каждом из тегов OBJECT привязанных элементов управления укажите значение DATAFLD, чтобы задать значения для данных, которые необходимо отобразить в каждом визуальном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-138">In each of the bound controls' OBJECT tags, specify the DATAFLD value to set the values for the data you want to display in each visual control.</span></span>

<span data-ttu-id="3ab8c-139">Ограничение количества **RDS не задано. Объекты DataControl,** которые можно встраить с помощью тегов OBJECT на одной веб-странице.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-139">There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single webpage.</span></span>

<span data-ttu-id="3ab8c-140">Когда вы определяете **RDS. Для объекта DataControl** на веб-странице используйте значения nonzero **Height** и **Width,** такие как 1 (во избежание включения дополнительного пространства).</span><span class="sxs-lookup"><span data-stu-id="3ab8c-140">When you define the **RDS.DataControl** object on a webpage, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>

<span data-ttu-id="3ab8c-141">Клиентские компоненты удаленной службы данных уже включены в состав Internet Explorer 4.0; Поэтому нет необходимости включать параметр CODEBASE в **RDS. Тег объекта DataControl.**</span><span class="sxs-lookup"><span data-stu-id="3ab8c-141">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you don't need to include a CODEBASE parameter in your **RDS.DataControl** object tag.</span></span>

<span data-ttu-id="3ab8c-142">С помощью Internet Explorer 4.0 или более поздней можно привязать данные с помощью htmL-элементов управления и ActiveX элементов управления, только если они помечены как элементы управления моделью apartment.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-142">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX controls only if they are marked as apartment model controls.</span></span>

<span data-ttu-id="3ab8c-143">**Microsoft Visual Basic пользователей** The **RDS. DataControl** используется только в веб-приложениях.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-143">**Microsoft Visual Basic Users** The **RDS.DataControl** is used only in web-based applications.</span></span> <span data-ttu-id="3ab8c-144">Клиентские Visual Basic не требуются.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-144">A Visual Basic client application has no need for it.</span></span>

