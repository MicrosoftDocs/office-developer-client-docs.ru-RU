---
title: Свойство Server (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f35910591d86e0e5a2b92d680be3c5f64504088
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308689"
---
# <a name="server-property-rds"></a>Свойство Server (RDS)

**Область применения**: Access 2013, Office 2013

Указывает имя служб IIS и протокол связи.

Свойство **Server** можно задать во время создания в элементе [ActiveX RDS. ](datacontrol-object-rds.md)Объектные теги объекта DataObject или во время выполнения в коде скрипта.

## <a name="syntax"></a>Синтаксис

|Протокол|Синтаксис времени конструирования|
|:-------|:-----------------|
|HTTP|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|HTTPS|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|ТРАФИК|`<PARAM NAME="Server" VALUE="computername">`|
|Внутрипроцессный|`<PARAM NAME="Server" VALUE="">`|


|Протокол|Синтаксис времени выполнения|
|:-------|:--------------|
|HTTP|`DataControl.Server="https://awebsrvr:port"`|
|HTTPS|`DataControl.Server="https://awebsrvr:port"`|
|ТРАФИК|`DataControl.Server="computername"`|
|Внутрипроцессный|`DataControl.Server=""`|


## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*авебсрвр* или *ComputerName* |**Строковое** значение, содержащее путь в Интернете или интрасети, или имя компьютера, если сервер находится на удаленном компьютере; или пустая строка, если сервер находится на локальном компьютере.|
|*порта* |Необязательный атрибут. Порт, используемый для подключения к серверу IIS. Номер порта задается в Internet Explorer (в меню **Сервис** выберите пункт **Свойства браузера**, а затем перейдите на вкладку **Подключение** ) или в IIS.|
|*DataControl* |Объектная переменная, представляющая **RDS. Объект управления** DataObject.|

## <a name="remarks"></a>Замечания

Сервер — это расположение, в котором **RDS. **Обрабатывается запрос на получение доступа к управлению запросами (то есть запрос или обновление). По умолчанию все запросы обрабатываются объектом [рдссервер.](datafactory-object-rdsserver.md) DataObject, [мсдфмап. ](datafactory-customization.md)Компонент обработчика и [мсдфмап. INI](understanding-the-customization-file.md) -файл на указанном сервере. 

Помните, что при изменении серверов для согласования параметров в старых и новых **мсдфмап. INI** -файлы. Несовместимость может привести к сбою запросов, которые успешно выполняются на одном сервере. Если для свойства Server задано значение "", эти объекты будут использоваться на локальном компьютере.

