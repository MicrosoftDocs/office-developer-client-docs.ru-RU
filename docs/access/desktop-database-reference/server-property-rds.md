---
title: Свойство сервера (RDS)
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
# <a name="server-property-rds"></a>Свойство сервера (RDS)

**Область применения**: Access 2013, Office 2013

Указывает имя служб IIS и протокол связи.

Вы можете настроить свойство **Server** во время разработки в [RDS. Теги](datacontrol-object-rds.md) OBJECT объекта DataControl или во время запуска в коде скриптов.

## <a name="syntax"></a>Синтаксис

|Протокол|Синтаксис времени разработки|
|:-------|:-----------------|
|HTTP|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|HTTPS|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|DCOM|`<PARAM NAME="Server" VALUE="computername">`|
|В процессе|`<PARAM NAME="Server" VALUE="">`|


|Протокол|Синтаксис времени запуска|
|:-------|:--------------|
|HTTP|`DataControl.Server="https://awebsrvr:port"`|
|HTTPS|`DataControl.Server="https://awebsrvr:port"`|
|DCOM|`DataControl.Server="computername"`|
|В процессе|`DataControl.Server=""`|


## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*awebsrvr* или *имя компьютера* |**Строка,** которая содержит путь к Интернету или интрасети или имя компьютера, если сервер находится на удаленном компьютере; или пустую строку, если сервер находится на локальном компьютере.|
|*port* |Необязательный параметр. Порт, используемый для подключения к серверу IIS. Номер порта устанавливается в Internet Explorer (в меню "Инструменты"  щелкните "Параметры браузера" и выберите вкладку "Подключение") или в IIS. |
|*DataControl* |Объектная переменная, представляюная **RDS. Объект DataControl.**|

## <a name="remarks"></a>Заметки

Сервер — это расположение, в котором находится **RDS. Обработка запроса DataControl** (то есть запроса или обновления). По умолчанию все запросы обрабатываются объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) [MSDFMAP. Компонент обработки](datafactory-customization.md) и [MSDFMAP.INI](understanding-the-customization-file.md) на указанном сервере. 

Помните, что при изменении серверов для согласования параметров в старых и **MSDFMAP.INI** файлов. Несовместимость может привести к сбойу запросов, которые были успешно на одном сервере, на другом. Если для свойства Server установлено "", эти объекты будут использоваться на локальном компьютере.

