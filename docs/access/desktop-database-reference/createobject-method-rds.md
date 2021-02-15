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

Создает прокси для целевого бизнес-объекта и возвращает на него указатель. Прокси-сервер упаковывает и маршалит данные на серверной загоне для связи с бизнес-объектом для отправки запросов и данных через Интернет. Для объектов компонентов, используемых в процессе, прокси не используются, предоставляется только указатель на объект.

## <a name="syntax"></a>Синтаксис

Удаленная служба данных поддерживает следующие протоколы: HTTP, HTTPS (http over Secure Socket Layer), DCOM и в процессе.

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
<td><p>Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p>Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p>Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>computername</em> &quot; )</p></td>
</tr>
<tr class="even">
<td><p>In-process</p></td>
<td><p>Set<em>object</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; &quot; )</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Object* |Объектная переменная, оцениваемая для объекта, который является типом, указанным в *ProgID.*|
|*DataSpace* |Объектная переменная, представляюная [RDS. Объект DataSpace,](dataspace-object-rds.md) используемый для создания экземпляра нового объекта.|
|*ProgID* |**Строка,** которая содержит программный идентификатор, определяющий серверный бизнес-объект, реализующий бизнес-правила приложения.|
|*awebsrvr* или *имя компьютера* |**Строковые** значения, которые представляют URL-адрес, идентифицирующий веб-сервер служб IIS, на котором создается экземпляр бизнес-объекта сервера.|

## <a name="remarks"></a>Заметки

Протокол *HTTP является* стандартным веб-протоколом; *HTTPS* — это безопасный веб-протокол. Используйте протокол *DCOM при* запуске локальной сети без протокола HTTP. Этот *протокол является* локальной библиотекой динамической ссылки (DLL); Он не использует сеть.

