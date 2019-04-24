---
title: Объект управления объектами (RDS)
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
# <a name="datacontrol-object-rds"></a><span data-ttu-id="91a69-102">Объект управления объектами (RDS)</span><span class="sxs-lookup"><span data-stu-id="91a69-102">DataControl object (RDS)</span></span>

<span data-ttu-id="91a69-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91a69-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91a69-104">Связывает [набор записей](recordset-object-ado.md) запроса данных с одним или несколькими элементами управления (например, текстовым полем, элементом управления сетки или полем со списком) для отображения данных **набора записей** на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="91a69-104">Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a webpage.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a69-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91a69-105">Syntax</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a><span data-ttu-id="91a69-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="91a69-106">Remarks</span></span>

<span data-ttu-id="91a69-107">Идентификатор класса для \*\*RDS. \*\*Объект BD96C556-65A3-11D0-983A-00C04FC29E33.</span><span class="sxs-lookup"><span data-stu-id="91a69-107">The class ID for the **RDS.DataControl** object is BD96C556-65A3-11D0-983A-00C04FC29E33.</span></span>

> [!NOTE]
> <span data-ttu-id="91a69-108">Если вы получаете сообщение об ошибке [RDS. Пространство](dataspace-object-rds.md) или \*\*RDS. \*\*Не загружен объект элемента управления, убедитесь, что используется правильный идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="91a69-108">If you get an error that an [RDS.DataSpace](dataspace-object-rds.md) or **RDS.DataControl** object doesn't load, make sure you are using the correct class ID.</span></span> <span data-ttu-id="91a69-109">Идентификаторы классов для этих объектов изменились с версии 1,0 и 1,1.</span><span class="sxs-lookup"><span data-stu-id="91a69-109">The class IDs for these objects have changed from version 1.0 and 1.1.</span></span>

<span data-ttu-id="91a69-110">Для базового сценария необходимо задать только свойства **SQL**, **Connect**и **Server** объекта \*\*RDS. \*\*Объект DataObject, который автоматически вызывает объект [рдссервер.](datafactory-object-rdsserver.md)DataObject, используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91a69-110">For a basic scenario, you need to set only the **SQL**, **Connect**, and **Server** properties of the **RDS.DataControl** object, which will automatically call the default business object, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span></span>

<span data-ttu-id="91a69-111">Все свойства в **RDS. Элемент управления** не является обязательным, так как пользовательские бизнес-объекты могут заменять свои функции.</span><span class="sxs-lookup"><span data-stu-id="91a69-111">All the properties in the **RDS.DataControl** are optional because custom business objects can replace their functionality.</span></span>

> [!NOTE]
> <span data-ttu-id="91a69-112">Если вы запрашиваете несколько результатов, возвращается только первый [набор записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="91a69-112">If you query for multiple results, only the first [Recordset](recordset-object-ado.md) is returned.</span></span> <span data-ttu-id="91a69-113">Если требуется несколько наборов результатов, назначьте каждый из них отдельному **элементу управления**.</span><span class="sxs-lookup"><span data-stu-id="91a69-113">If multiple result sets are needed, assign each to its own **DataControl**.</span></span> 
> 
> <span data-ttu-id="91a69-114">Ниже `"Select * from Authors, Select * from Topics"`приведен пример запроса для нескольких результатов.</span><span class="sxs-lookup"><span data-stu-id="91a69-114">An example of a query for multiple results could be the following: `"Select * from Authors, Select * from Topics"`.</span></span>

<span data-ttu-id="91a69-115">Добавление "Дфмоде = 20;" в строку подключения при использовании **RDS. Объект управления** данными может увеличить производительность сервера при обновлении данных.</span><span class="sxs-lookup"><span data-stu-id="91a69-115">Adding "DFMode=20;" to your connection string when using the **RDS.DataControl** object can improve your server's performance when updating data.</span></span> <span data-ttu-id="91a69-116">При использовании этого параметра объект **фактического объекта рдссервер.** DataObject на сервере использует менее ресурсоемкий режим.</span><span class="sxs-lookup"><span data-stu-id="91a69-116">With this setting, the **RDSServer.DataFactory** object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="91a69-117">Однако следующие функции недоступны в этой конфигурации:</span><span class="sxs-lookup"><span data-stu-id="91a69-117">However, the following features are not available in this configuration:</span></span>

  - <span data-ttu-id="91a69-118">Использование параметризованных запросов.</span><span class="sxs-lookup"><span data-stu-id="91a69-118">Using parameterized queries.</span></span>

  - <span data-ttu-id="91a69-119">Получить сведения о параметрах или столбцах перед вызовом метода **EXECUTE** .</span><span class="sxs-lookup"><span data-stu-id="91a69-119">Getting parameter or column information before calling the **Execute** method.</span></span>

  - <span data-ttu-id="91a69-120">Установка значения **true**для **обновлений Transact** .</span><span class="sxs-lookup"><span data-stu-id="91a69-120">Setting **Transact Updates** to **True**.</span></span>

  - <span data-ttu-id="91a69-121">Получает состояние строки.</span><span class="sxs-lookup"><span data-stu-id="91a69-121">Getting row status.</span></span>

  - <span data-ttu-id="91a69-122">Вызов метода [Resync](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="91a69-122">Calling the [Resync](resync-method-ado.md) method.</span></span>

  - <span data-ttu-id="91a69-123">Обновление (явно или автоматически) с помощью [](update-resync-property-dynamic-ado.md) свойства Resync.</span><span class="sxs-lookup"><span data-stu-id="91a69-123">Refreshing (explicitly or automatically) via the [Update Resync](update-resync-property-dynamic-ado.md) property.</span></span>

  - <span data-ttu-id="91a69-124">Задание свойств **команды** или [набора записей](recordset-sourcerecordset-properties-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="91a69-124">Setting **Command** or [Recordset](recordset-sourcerecordset-properties-rds.md) properties.</span></span>

  - <span data-ttu-id="91a69-125">С помощью **адкмдтабледирект**.</span><span class="sxs-lookup"><span data-stu-id="91a69-125">Using **adCmdTableDirect**.</span></span>

<span data-ttu-id="91a69-126">**RDS. Объект элемента управления** данные по умолчанию работает в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="91a69-126">The **RDS.DataControl** object runs in asynchronous mode by default.</span></span> <span data-ttu-id="91a69-127">Если для приложения требуется синхронное выполнение, задайте для параметра [ExecuteOptions](executeoptions-property-rds.md) значение **адцексексинк** , а для параметра [FetchOptions](fetchoptions-property-rds.md) — значение **адкфетчупфронт**, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="91a69-127">If you require synchronous execution for your application, set the [ExecuteOptions](executeoptions-property-rds.md) parameter equal to **adcExecSync** and the [FetchOptions](fetchoptions-property-rds.md) parameter equal to **adcFetchUpFront**, as shown in the following example.</span></span>

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

<span data-ttu-id="91a69-128">Использование одной **RDS. Объект элемента управления** DataObject для связывания результатов одного запроса с одним или несколькими визуальными элементами управления.</span><span class="sxs-lookup"><span data-stu-id="91a69-128">Use one **RDS.DataControl** object to link the results of a single query to one or more visual controls.</span></span> <span data-ttu-id="91a69-129">Например, предположим, что вы запрашиваете запрос на получение данных о клиентах, таких как имя, название проживания, место рождения, возраст и приоритет клиентов.</span><span class="sxs-lookup"><span data-stu-id="91a69-129">For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status.</span></span> <span data-ttu-id="91a69-130">Вы можете использовать одну и ту же **RDS. Объект управления** DataObject для отображения имени, возраста и региона клиента в трех отдельных текстовых полях; Приоритет — состояние клиентов в флажке; и все данные в элементе управления Grid.</span><span class="sxs-lookup"><span data-stu-id="91a69-130">You can use a single **RDS.DataControl** object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</span></span>

<span data-ttu-id="91a69-131">Использование различных **RDS. Объекты управления** объектами для связывания результатов нескольких запросов с различными визуальными элементами управления.</span><span class="sxs-lookup"><span data-stu-id="91a69-131">Use different **RDS.DataControl** objects to link the results of multiple queries to different visual controls.</span></span> <span data-ttu-id="91a69-132">Например, предположим, что вы используете один запрос для получения сведений о клиенте, а второй — для получения сведений о приобретенных товарах, приобретенных клиентом.</span><span class="sxs-lookup"><span data-stu-id="91a69-132">For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased.</span></span> <span data-ttu-id="91a69-133">Вы хотите отобразить результаты первого запроса в трех текстовых полях и один флажок, а также результаты второго запроса в элементе управления "Grid".</span><span class="sxs-lookup"><span data-stu-id="91a69-133">You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control.</span></span> <span data-ttu-id="91a69-134">Если вы используете бизнес-объект по умолчанию (**рдссервер.** DataObject), необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="91a69-134">If you use the default business object (**RDSServer.DataFactory**), you need to do the following:</span></span>

  - <span data-ttu-id="91a69-135">Добавление двух **служб RDS. Объекты управления** на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="91a69-135">Add two **RDS.DataControl** objects to your webpage.</span></span>

  - <span data-ttu-id="91a69-136">Напишите два запроса: по одному для каждого свойства **SQL** двух **служб RDS. Объекты управления** объектами.</span><span class="sxs-lookup"><span data-stu-id="91a69-136">Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects.</span></span> <span data-ttu-id="91a69-137">Одна **RDS. Объект элемента управления** данными будет содержать запрос SQL, запрашивающий сведения о клиенте; Вторая будет содержать запрос на получение списка приобретенных товаров у клиента.</span><span class="sxs-lookup"><span data-stu-id="91a69-137">One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</span></span>

  - <span data-ttu-id="91a69-138">В каждом из тегов объекта привязанных элементов управления укажите значение ДАТАФЛД, чтобы задать значения для данных, которые будут отображаться в каждом визуальном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="91a69-138">In each of the bound controls' OBJECT tags, specify the DATAFLD value to set the values for the data you want to display in each visual control.</span></span>

<span data-ttu-id="91a69-139">Количество ограничений по количеству служб RDS не ограничено **. Объекты управления** объектами, которые можно внедрять с помощью тегов объекта на одной веб-странице.</span><span class="sxs-lookup"><span data-stu-id="91a69-139">There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single webpage.</span></span>

<span data-ttu-id="91a69-140">При определении службы **RDS. Объект элемента управления** данные на веб-странице используйте значения ненулевОй **высоты** и **ширины** , например 1 (чтобы избежать лишних пробелов).</span><span class="sxs-lookup"><span data-stu-id="91a69-140">When you define the **RDS.DataControl** object on a webpage, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>

<span data-ttu-id="91a69-141">Клиентские компоненты удаленной службы данных уже включены в состав Internet Explorer 4,0; Поэтому не нужно включать параметр CODEBASE в вашу службу **RDS. Тег объекта элемента управления** для объекта.</span><span class="sxs-lookup"><span data-stu-id="91a69-141">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you don't need to include a CODEBASE parameter in your **RDS.DataControl** object tag.</span></span>

<span data-ttu-id="91a69-142">С помощью Internet Explorer 4,0 или более поздней версии можно выполнять привязывание к данным с помощью элементов управления HTML и элементов управления ActiveX, только если они помечены как элементы управления модели подразделения.</span><span class="sxs-lookup"><span data-stu-id="91a69-142">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX controls only if they are marked as apartment model controls.</span></span>

<span data-ttu-id="91a69-143">**Пользователи Microsoft Visual Basic** **RDS. Элемент управления** данных используется только в веб-приложениях.</span><span class="sxs-lookup"><span data-stu-id="91a69-143">**Microsoft Visual Basic Users** The **RDS.DataControl** is used only in web-based applications.</span></span> <span data-ttu-id="91a69-144">Для клиентского приложения Visual Basic это не требуется.</span><span class="sxs-lookup"><span data-stu-id="91a69-144">A Visual Basic client application has no need for it.</span></span>

