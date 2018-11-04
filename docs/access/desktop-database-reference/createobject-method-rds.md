---
title: Метод CreateObject (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f622ee94fa6e37c2f618b038aea746791e58e9b8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950085"
---
# <a name="createobject-method-rds"></a>Метод CreateObject (RDS)

**Применимо к**: Access 2013, Office 2013

Создает прокси-сервера для бизнес-конечного объекта и возвращает указатель на него. Прокси-сервер пакеты и выполняет маршалинг данные на стороне сервера заглушку взаимодействие с бизнес-объект для отправки запросов и данных через Интернет. Для объектов в процесс компонент не прокси-серверы используются, если только указатель на объект.

## <a name="syntax"></a>Синтаксис

Служба удаленных данных поддерживает следующие протоколы: HTTP, HTTPS (HTTP через протокол SSL), DCOM и в процессе.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Протокол</p></th>
<th><p>Синтаксис</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>HTTP</p></td>
<td><p>Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p>Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p>Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>computername</em>&quot;)</p></td>
</tr>
<tr class="even">
<td><p>В работе</p></td>
<td><p>Установить для<em>объекта</em> = <em>пространства данных</em>. Функция CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Объект* |Объектная переменная, которое оценивается как объект, тип которого указан *идентификатор ProgID*.|
|*Пространства данных* |Объектную переменную, которая представляет [RDS. Пространства данных](dataspace-object-rds.md) используется для создания экземпляра объекта новый объект.|
|*ProgID* |**Строковое** значение, содержащее программный идентификатор, указав на сервере бизнес-объект, который реализует приложения бизнес-правил.|
|*awebsrvr* или *имя компьютера* |**Строковое** значение, представляющее URL-адрес, идентифицирующий веб-сервер Internet Information Services (IIS), где создается экземпляр объекта business server.|

## <a name="remarks"></a>Примечания

*Протокол HTTP* используется стандартный Интернет-протокола; *HTTPS* — это безопасный протокол. Используйте *протокол DCOM* при выполнении локальной сети без HTTP. Протокол *в процесс* является локальной библиотеки динамической компоновки (DLL); сети не используется.

