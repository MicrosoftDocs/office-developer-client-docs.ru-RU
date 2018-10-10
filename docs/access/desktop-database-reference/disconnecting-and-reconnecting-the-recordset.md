---
title: Disconnecting and Reconnecting the Recordset
TOCTitle: Disconnecting and Reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90435606bb0b3059f5769c12fe7cf3cac0c8f9f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483079"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>Disconnecting and Reconnecting the Recordset


**Применимо к**: Access 2013 | Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>Disconnecting and Reconnecting the Recordset

Одно из наиболее эффективные функции, доступные в ADO — это возможность открыть со стороны клиента **набора записей** из источника данных и затем *Отключите* **набора записей** из источника данных. После отключения **записей** подключения к источнику данных можно будет закрыто, тем самым освобождения ресурсов на сервере, используемое для поддержки его. Можно продолжить просмотр и изменение данных в **набор записей** во время его отключения и последующего повторного подключения к источнику данных и отправка обновлений в пакетном режиме.

Чтобы прервать **записей**, откройте его с расположения курсора из **adUseClient**и задайте для свойства **ActiveConnection** значение *Nothing*. (C++ пользователи должны задавать **ActiveConnection** равно NULL для отключения.)

Мы используем отключенного **набора записей** далее в этой главе при обсуждении хранение **записей** для решения проблемы, в котором нужно обновлять данные в **набор записей** для приложения, пока на клиентском компьютере не подключен к сети.
