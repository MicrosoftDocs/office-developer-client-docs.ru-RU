---
title: Метод CreateObject (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295375"
---
# <a name="createobject-method-rds"></a>Метод CreateObject (RDS)

**Область применения**: Access 2013, Office 2013

Создает прокси-сервер для целевого бизнес-объекта и возвращает ему указатель. Прокси-пакеты и маршалы данных в серверную загонку для связи с бизнес-объектом для отправки запросов и данных через Интернет. Для используемых в процессе объектов компонентов не используются прокси, только указка на объект предоставляется.

## <a name="syntax"></a>Синтаксис

Служба удаленных данных поддерживает следующие протоколы: HTTP, HTTPS (http over Secure Socket Layer), DCOM и in-process.

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
<td><p>Установите<em>объект</em>  =  <em>DataSpace</em>. CreateObject &quot; <em>(ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p>Установите<em>объект</em>  =  <em>DataSpace</em>. CreateObject &quot; <em>(ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p>Установите<em>объект</em>  =  <em>DataSpace</em>. CreateObject &quot; <em>(ProgId</em> &quot; , &quot; <em>computername</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>В процессе</p></td>
<td><p>Установите<em>объект</em>  =  <em>DataSpace</em>. CreateObject &quot; <em>(ProgId</em> &quot; , &quot; &quot; )</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Object* |Переменная объекта, которая оценивает объект, который является типом, указанным в *ProgID.*|
|*DataSpace* |Переменная объекта, представляюая [RDS. Объект DataSpace,](dataspace-object-rds.md) используемый для создания экземпляра нового объекта.|
|*ProgID* |Значение **String,** содержаное программный идентификатор, указывающий бизнес-объект на стороне сервера, реализующий бизнес-правила приложения.|
|*awebsrvr или* *computername* |Значение **String,** представляю которое представляет URL-адрес, идентифицирующий веб-сервер службы IIS (IIS), на котором создается экземпляр бизнес-объекта сервера.|

## <a name="remarks"></a>Примечания

Протокол *HTTP является* стандартным веб-протоколом; *HTTPS* — это безопасный веб-протокол. Используйте протокол *DCOM при* работе с локальной сетью без HTTP. Протокол *в процессе —* это локализованная библиотека динамических ссылок (DLL); он не использует сеть.

