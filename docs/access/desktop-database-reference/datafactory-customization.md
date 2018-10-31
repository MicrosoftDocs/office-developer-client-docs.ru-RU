---
title: Настройка DataFactory
TOCTitle: DataFactory Customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f058dd76d9ae4f95b6a3d051e741039eb7609f5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860870"
---
# <a name="datafactory-customization"></a>Настройка DataFactory


**Применимо к**: Access 2013 | Office 2013

Службы удаленных данных (RDS) позволяет легко осуществлять доступ к данным в системе с трехуровневой клиента и сервера. Данные клиентского элемента управления определяет подключение и параметры командной строки для выполнения запросов к удаленному источнику данных, или строку подключения и параметры объекта [набора записей](recordset-object-ado.md) для выполнения обновления.

Параметры передаются в программу сервера, который выполняет операцию доступа к данным к удаленному источнику данных. Служб удаленных рабочих СТОЛОВ предоставляет программы сервера по умолчанию, называется объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) . Объект **RDSServer.DataFactory** возвращает любого объекта **набора записей** , создаваемых в запрос для клиента.

Тем не менее, **RDSServer.DataFactory** ограничено для выполнения запросов и обновлений. Он не может выполнять любые проверки или обработки на подключение или командной строки.

С помощью ADO можно указать, что рабочий **DataFactory** совместно с другого типа программы сервера вызваны *обработчика*. Обработчик можно изменить подключение к клиенту и командной строки перед их использования для доступа к источнику данных. Кроме того обработчик может задать права доступа, которые управляют возможности клиента для чтения и записи данных в источник данных.

В разделах файл настройки заданы параметры, которые обработчик использует, чтобы изменить параметры клиента и прав доступа.

В следующих разделах Дополнительные сведения о настройке **DataFactory** объектов:

  - [Общие сведения о файле настройки](understanding-the-customization-file.md)

  - [Раздел Connect в файле настройки](customization-file-connect-section.md)

  - [Раздел SQL в файле настройки](customization-file-sql-section.md)

  - [Раздел UserList в файле настройки](customization-file-userlist-section.md)

  - [Раздел Logs в файле настройки](customization-file-logs-section.md)

  - [Параметры необходимые клиента](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)

  - [Создание настраиваемого обработчика](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
