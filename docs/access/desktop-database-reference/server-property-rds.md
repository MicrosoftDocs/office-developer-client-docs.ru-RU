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

Указывает имя службы IIS (IIS) и протокол связи.

Свойство Server **можно** задать во время разработки в [RDS. Объектные теги объекта DataControl](datacontrol-object-rds.md) или во время запуска в коде скриптов.

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
|*awebsrvr или* *computername* |Значение **String,** которое содержит путь к Интернету или интрасети или имя компьютера, если сервер находится на удаленном компьютере; или пустая строка, если сервер находится на локальном компьютере.|
|*порт* |Необязательный параметр. Порт, используемый для подключения к серверу IIS. Номер порта устанавливается в Internet Explorer (в меню **Tools** щелкните **Параметры** Интернета, а затем выберите вкладку **Подключение)** или в IIS.|
|*DataControl* |Переменная объекта, представляюая **RDS. Объект DataControl.**|

## <a name="remarks"></a>Примечания

Сервер — это расположение, в котором находится **RDS. Обрабатывается запрос DataControl** (то есть запрос или обновление). По умолчанию все запросы обрабатываются объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) [MSDFMAP. Компонент обработка](datafactory-customization.md) и [MSDFMAP.INI](understanding-the-customization-file.md) файл на указанном сервере. 

Помните, что при изменении серверов для  согласования параметров в старыхMSDFMAP.INIфайлах. Несовместимость может привести к сбойу запросов на одном сервере на другом. Если свойство Server настроено на "", эти объекты будут использоваться на локальной машине.

