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

Если после обновления до Windows 2000 возникают трудности с правильной работу RDS, выполните следующие действия, чтобы устранить проблему.

1.  Убедитесь, что в первую очередь запущена служба веб-публикаций, переехав на https://*с* помощью Internet Explorer. Если вам не удается получить доступ к веб-серверу таким образом, перейдите в командную команду и введите следующую команду: "NET START W3SVC".

2.  В меню "Пуск" выберите "Выполнить". Введите msdfmap.ini и нажмите кнопку ОК, чтобы открыть msdfmap.ini в Блокноте. Проверьте раздел CONNECT DEFAULT и, если параметр ACCESS имеет значение \[ NOACCESS, измените его на \] READONLY.

3.  С помощью программы RegEdit перейдите в "HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ DataFactory \\ HandlerInfo"  и убедитесь, что для **HandlerRequired** установлено значение 0, а для DefaultHandler — "" (строка NULL).
    
    > [!NOTE]
    > При внесении каких-либо изменений в этот раздел реестра необходимо остановить и перезапустить службу веб-публикации, введите следующие команды в командной области: "NET STOP W3SVC" и "NET START W3SVC".

4.  С помощью Служебная программа RegEdit перейдите в реестр к "HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet Services W3SVC Parameters ADCLaunch" и убедитесь, что есть ключ \\ \\ \\ \\ **RDSServer.Datafactory**. Если нет, создайте его.

5.  С помощью диспетчера служб Интернета перейдите на веб-сайт по умолчанию и просмотрете свойства виртуального корня MSADC. Проверьте ограничения безопасности и IP-адреса каталога и доменных имен. Если проверяется "Доступ отказано", выберите "Предоставлено".

Попробуйте перезагрузать сервер, если изменения не появятся, чтобы решить проблему.

