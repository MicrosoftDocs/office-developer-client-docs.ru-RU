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

Создает прокси-сервер для целевого бизнес-объекта и возвращает указатель на него. Пакеты прокси-сервера и маршалирует данные в заглушку на стороне сервера для связи с бизнес-объектами для отправки запросов и данных через Интернет. Для объектов внутрипроцессного компонента не используются прокси-серверы, предоставляется только указатель на этот объект.

## <a name="syntax"></a>Синтаксис

Удаленная служба данных поддерживает следующие протоколы: HTTP, HTTPS (HTTP over SSL Layer), DCOM и внутрипроцессный.

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
<td><p>Задайте<em>объектное</em> = <em>пространство</em>. CreateObject (&quot;<em>ProgID</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p>Задайте<em>объектное</em> = <em>пространство</em>. CreateObject (&quot;<em>ProgID</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</p></td>
</tr>
<tr class="odd">
<td><p>ТРАФИК</p></td>
<td><p>Задайте<em>объектное</em> = <em>пространство</em>. CreateObject (&quot;<em>ProgID</em>&quot;, &quot; <em>ComputerName</em>&quot;)</p></td>
</tr>
<tr class="even">
<td><p>Внутрипроцессный</p></td>
<td><p>Задайте<em>объектное</em> = <em>пространство</em>. CreateObject (&quot;<em>ProgID</em>&quot;, &quot; &quot;)</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Object* |Объектная переменная, которая оценивается как объект, который является типом, указанным в параметре *ProgID*.|
|*DataSpace* |Объектная переменная, представляющая [RDS. Объект Space](dataspace-object-rds.md) , используемый для создания экземпляра нового объекта.|
|*ProgID* |**Строковое** значение, содержащее программный идентификатор, указывающий на серверный бизнес-объект, который реализует бизнес-правила приложения.|
|*авебсрвр* или *ComputerName* |**Строковое** значение, представляющее URL-адрес, определяющий веб-сервер служб IIS, на котором создается экземпляр бизнес-объекта сервера.|

## <a name="remarks"></a>Примечания

*Http-протокол* является стандартным веб-протоколом; *HTTPS* — это безопасный веб-протокол. Используйте *протокол DCOM* при работе с локальной сетью без протокола HTTP. *Внутрипроцессный* протокол — это локальная библиотека динамической КОМПОНОВКИ (DLL); она не использует сеть.

