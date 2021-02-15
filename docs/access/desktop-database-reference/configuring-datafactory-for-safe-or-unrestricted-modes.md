---
title: Configuring DataFactory for Safe or Unrestricted Modes
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4313d48359499eaf249a68eb97408c8ed4ecb88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295998"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a>Configuring DataFactory for Safe or Unrestricted Modes


**Область применения**: Access 2013, Office 2013

По умолчанию ADO устанавливается с "безопасной" [конфигурацией RDSServer.DataFactory.](datafactory-object-rdsserver.md) Безопасный режим для компонентов сервера RDS означает, что истинны следующие:

1.  Обработчик необходим для RDSServer.DataFactory (это задано параметром ключа реестра).

2.  Обработтель по умолчанию, msdfmap.handler, зарегистрирован, присутствует в списке безопасных обработщиков и помечен как обработтель по умолчанию.

3.  Msdfmap.ini файл установлен в каталоге Windows. Этот файл необходимо настроить в соответствии с потребностями, прежде чем использовать RDS в трехуровневом режиме.

При желании можно настроить неоконфигурированную **установку DataFactory.** **DataFactory** можно использовать напрямую без настраиваемого обработчика. Пользователи по-прежнему могут использовать настраиваемый обработок, изменяя строки подключения, но это не требуется. Дополнительные сведения о последствиях использования объекта **RDSServer.DataFactory** см. в подраздеке "Защита приложений [RDS".](securing-rds-applications.md)

Файл реестра handsafe.reg был предоставлен для настройки записей реестра обработок для безопасной конфигурации. Чтобы запустить в безопасном режиме, запустите handsafe.reg. Файл реестра handunsf.reg был предоставлен для настройки записей реестра обработителя для неограниченной конфигурации. Чтобы работать в неограниченном режиме, запустите handunsf.reg.

После запуска handsafe.reg или handunsf.reg необходимо остановить и перезапустить службу веб-публикации на веб-сервере, введя в командном окне следующие команды: "NET STOP W3SVC" и "NET START W3SVC".

Дополнительные сведения об использовании функции обработки настроек RDS см. в технической статье "Использование функции обработки настроек в RDS 2.1".

