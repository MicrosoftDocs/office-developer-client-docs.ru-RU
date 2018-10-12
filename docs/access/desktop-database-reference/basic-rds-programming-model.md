---
title: Basic RDS Programming Model
TOCTitle: Basic RDS Programming Model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a90423f6bd05ae3d721faf97291ea6d21aa4393
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481683"
---
# <a name="basic-rds-programming-model"></a>Basic RDS Programming Model


**Применимо к**: Access 2013 | Office 2013

Приложения, которые имеются в среде следующих решает служб удаленных рабочих СТОЛОВ: клиентское приложение задает программы, который будет выполняться на сервере и параметры, необходимые для возврата требуемой информации. Программа вызван для доступа к серверу прибыли для указанного источника данных, извлекает сведения о, при необходимости обрабатывает данные и затем возвращает результирующую сведения о клиентского приложения в форме, его можно легко использовать. Служб удаленных рабочих СТОЛОВ предоставляет средства, которые необходимо выполнить следующую последовательность действий:

  - Укажите программу для вызова на сервере и получить способ обращения к нему из клиента. (Этот справочник иногда называется *прокси-сервера*. Представляет программу удаленного сервера. Клиентское приложение «вызовет» прокси-сервер как если бы были локальной программы, но он вызывает программу удаленного сервера.)

  - Вызов программы сервера. Передайте параметры идентификации источника данных и команды на выполнение программы-сервера. (Серверная программа использует ADO для получения доступа к источнику данных. ADO подключается к один из заданных параметров и затем выдает команды, указанной в параметре other.)

  - Программа сервера получает объект [набора записей](recordset-object-ado.md) из источника данных. Кроме того в объект **набора записей** обрабатывается на сервере.

  - Программы сервера возвращает окончательный объекта **набора записей** для клиентского приложения.

  - В клиенте объекта **набора записей** помещается в форму, можно легко использовать визуальные элементы управления.

  - Каких-либо изменений в объект **набора записей** , передаются в программу сервера, который использует их для обновления источника данных.

В этой программной модели содержит элементы, определенные удобства. Если нет необходимости программы сложных сервера для доступа к источнику данных, и в случае предоставления требуемое подключение и параметры команды служб удаленных рабочих СТОЛОВ будут автоматически получить данные, указанного с помощью простой, программы сервера по умолчанию.

Если вам требуется более сложных обработки, можно указать настраиваемый серверный программы. Например так как программа настраиваемый серверный имеет все возможности ADO в его распоряжении, его может подключаться к нескольким источникам данных, объединить их данные сложных каким-либо образом и возвращается результат простой, обработанные клиентское приложение.

И, наконец Если вашим требованиям, где-то между ADO теперь поддерживает настройки поведения программы сервера по умолчанию.
