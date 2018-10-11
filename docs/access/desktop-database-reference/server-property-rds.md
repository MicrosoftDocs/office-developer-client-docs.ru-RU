---
title: Server Property (RDS)
TOCTitle: Server Property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec001c57f72582dcdaabdfd6e76069582468b54c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479812"
---
# <a name="server-property-rds"></a>Server Property (RDS)


**Применимо к**: Access 2013 | Office 2013

Указывает имя и связи протокол Internet Information Services (IIS).

Свойства **сервера** во время разработки в [RDS. DataControl](datacontrol-object-rds.md) теги OBJECT объекта, или во время выполнения в коде сценария.

## <a name="syntax"></a>Синтаксис

|Протокол|Синтаксис во время разработки|
|:-------|:-----------------|
|HTTP|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|HTTPS|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|DCOM|`<PARAM NAME="Server" VALUE="computername">`|
|В работе|`<PARAM NAME="Server" VALUE="">`|


|Протокол|Синтаксис во время выполнения|
|:-------|:--------------|
|HTTP|`DataControl.Server="https://awebsrvr:port"`|
|HTTPS|`DataControl.Server="https://awebsrvr:port"`|
|DCOM|`DataControl.Server="computername"`|
|В работе|`DataControl.Server=""`|


## <a name="parameters"></a>Параметры

*awebsrvr* или *имя компьютера*

- **Строковое** значение, содержащее Интернет или интрасети путь или имя компьютера, если сервер на удаленном компьютере; или же пустая строка, если сервер не на локальном компьютере.

*порт*

- Необязательный параметр. Порт, используемый для подключения к серверу службы IIS. Номер порта задано в Internet Explorer (в меню **Сервис** выберите пункт **Свойства обозревателя**и перейдите на вкладку **подключения** ) или в службах IIS.

*DataControl*

- Объектную переменную, которая представляет **RDS. DataControl** объекта.

## <a name="remarks"></a>Замечания

Сервер — это местоположение где **RDS. DataControl** обработки запроса (то есть, запроса или обновления). По умолчанию все запросы обрабатываются с помощью объекта [RDSServer.DataFactory](datafactory-object-rdsserver.md) , [MSDFMAP. Обработчик](datafactory-customization.md) компонента и [MSDFMAP. INI](understanding-the-customization-file.md) файл на указанном сервере. 

Помните, что при изменении серверы для согласования параметров в старой и новой **MSDFMAP. INI** файлов. На совместимость может стать причиной запросов, которые выполняются успешно на одном сервере к сбою на другой. Если свойство сервера задано значение «», эти объекты будут использоваться на локальном компьютере.

