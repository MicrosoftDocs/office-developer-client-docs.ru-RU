---
title: Настройка RDS в Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8482df5ca2fab110e5b1a77fe227c5f0c583d893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296019"
---
# <a name="configuring-rds-on-windows-2000"></a>Настройка RDS в Windows 2000


**Область применения**: Access 2013, Office 2013

Если после обновления до 2000 года Windows RDS, выполните следующие действия, чтобы устранить проблему.

1.  Убедитесь, что служба публикации world Wide Web запущена сначала, перенавигавшись на https://*с* помощью Internet Explorer. Если таким образом вы не можете получить доступ к веб-серверу, перейдите к командной подсказке и введите следующую команду: "NET START W3SVC".

2.  Из меню "Пуск" выберите Выполнить. Введите msdfmap.ini и нажмите кнопку ОК, чтобы открыть msdfmap.ini в Блокнот. Проверьте раздел CONNECT DEFAULT, и если параметр ACCESS задан \[ \] в NOACCESS, измените его на READONLY.

3.  С помощью утилиты RegEdit перейдите в "HKEY \_ LOCAL MACHINE SOFTWARE Microsoft DataFactory HandlerInfo" и убедитесь, что значение \_ \\ \\ \\ \\ **HandlerRequired** равно 0, а **DefaultHandler** — "" (строка Null).
    
    > [!NOTE]
    > При внесении изменений в этот раздел реестра необходимо остановить и перезапустить службу публикации World Wide Web Publishing Service, введите следующие команды по командной подсказке: "NET STOP W3SVC" и "NET START W3SVC".

4.  Используя утилиту RegEdit, перейдите в реестр по ссылке "HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet Services W3SVC Parameters ADCLaunch" и убедитесь, что есть ключ под названием \\ \\ \\ \\ **RDSServer.Datafactory**. Если нет, создайте его.

5.  С помощью диспетчера интернет-служб перейдите на веб-сайт по умолчанию и просмотреть свойства виртуального корневого корня MSADC. Проверьте ограничения безопасности каталога и IP-адресов и доменных имен. Если "Доступ отказано" проверяется, выберите "Предоставлено".

Попробуйте перезагрузать сервер, если изменения сначала не решат проблему.

