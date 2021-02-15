---
title: Метод CopyRecord (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295529"
---
# <a name="copyrecord-method-ado"></a>Метод CopyRecord (ADO)

**Область применения**: Access 2013, Office 2013

Копирует объект, представленный **записью,** в другое расположение.

## <a name="syntax"></a>Синтаксис

*Запись*. CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Source* |Необязательный параметр. **Строка,** которая содержит URL-адрес, определяющий скопированную сущность (например, файл или каталог). Если *source* опущен или указывает пустую строку, файл или каталог, представленный текущей записью, [будет](record-object-ado.md) скопирован.|
|*Destination* |Необязательный параметр. **Строка,** содержаная URL-адрес, определяющий *расположение,* в которое будет скопирован источник.|
|*UserName* |Необязательный параметр. **Строка,** содержаная ид пользователя, который при необходимости разрешает доступ к пункту *назначения.*|
|*Password* |Необязательный параметр. Строковое значение, которое содержит пароль, который при необходимости проверяет *имя пользователя.* |
|*Options* |Необязательный параметр. Значение [CopyRecordOptionsEnum](copyrecordoptionsenum.md) со значением по умолчанию **adCopyUnspecified.** Указывает поведение этого метода.|
|*Async* |Необязательный параметр. **Boolean** value that, when **True,** specifies that this operation should be asynchronous.|

## <a name="return-value"></a>Возвращаемое значение

**Строка,** которая обычно возвращает значение *Destination.* Однако точное значение зависит от поставщика.

## <a name="remarks"></a>Заметки

Значения *"Источник"* и *"Назначение"* не должны быть идентичными; в противном случае возникает ошибка во время запуска. По крайней мере одно имя сервера, пути или ресурса должно отличаться.

Все children (например, subdirectories) source *копируется* рекурсивно, если не указан **adCopyNonRecursive.** В рекурсивной операции *назначение* не должно быть подкадектором *источника;* в противном случае операция не будет завершена.

Этот метод не удается, если *destination* идентифицирует существующую сущность (например, файл или каталог), если не указан **adCopyOverWrite.**

> [!IMPORTANT]
> Используйте **параметр adCopyOverWrite** тщательно. Например, при указании этого параметра при копировании файла в каталог каталог удаляется и заменяется файлом. 


> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)


