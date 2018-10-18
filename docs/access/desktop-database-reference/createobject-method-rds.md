---
title: CreateObject Method (RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ff2381626e8cf81aa95ee9d49f9396bd4b0316
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602722"
---
# <a name="createobject-method-rds"></a>CreateObject Method (RDS)


**Применимо к**: Access 2013 | Office 2013


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

  - *Объект*

  - Объектная переменная, которое оценивается как объект, тип которого указан *идентификатор ProgID*.

  - *Пространства данных*

  - Объектную переменную, которая представляет [RDS. Пространства данных](dataspace-object-rds.md) используется для создания экземпляра объекта новый объект.

  - *ProgID*

  - **Строковое** значение, содержащее программный идентификатор, указав на сервере бизнес-объект, который реализует приложения бизнес-правил.

  - *awebsrvr* или *имя компьютера*

<<<<<<< HEAD
  - **Строковое** значение, представляющее URL-адрес, идентифицирующий Internet Information Services (IIS) веб-сервере, где создается экземпляр объекта business server.

## <a name="remarks"></a>Замечания

<a name="the-http-protocol-is-the-standard-web-protocol-https-is-a-secure-web-protocol-use-the-dcom-protocol-when-running-a-local-area-network-without-http-the-in-process-protocol-is-a-local-dynamic-link-library-dll-it-does-not-use-a-network"></a>*Протокол HTTP* является протоколом Web; *HTTPS* является безопасной Интернет-протокола. Используйте *протокол DCOM* при выполнении локальной сети без HTTP. Протокол *в процесс* является локальной библиотеки динамической компоновки (DLL); сети не используется.
=======
  - **Строковое** значение, представляющее URL-адрес, идентифицирующий веб-сервер Internet Information Services (IIS), где создается экземпляр объекта business server.

## <a name="remarks"></a>Замечания

*Протокол HTTP* используется стандартный Интернет-протокола; *HTTPS* — это безопасный протокол. Используйте *протокол DCOM* при выполнении локальной сети без HTTP. Протокол *в процесс* является локальной библиотеки динамической компоновки (DLL); сети не используется.
>>>>>>> master

