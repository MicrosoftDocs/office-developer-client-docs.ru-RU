---
title: Метод CopyTo (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e8de2caf2abc53b0dbd014f21a85a6d54749033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295480"
---
# <a name="copyto-method-ado"></a>Метод CopyTo (ADO)

**Область применения**: Access 2013, Office 2013

Копирует указанное количество символов или ветвей (в зависимости от [типа)](type-property-ado-stream.md) [в потоке](stream-object-ado.md) в другой **объект Stream.**

## <a name="syntax"></a>Синтаксис

*Stream*. CopyTo *DestStream*, *NumChars*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DestStream* |Значение переменной объекта, которое содержит ссылку на открытый **объект Stream.** Текущий **поток** копируется в поток **назначения,** указанный *DestStream.* Поток назначения **должен** быть уже открыт. В этом случае возникает ошибка во время запуска.<br/><br/>**ПРИМЕЧАНИЕ.** Параметр *DestStream* может не быть прокси-сервером объекта **Stream,** так как для этого требуется доступ к частному интерфейсу в объекте **Stream,** который нельзя удаленно отоадлить от клиента.|
|*NumChars* |Необязательный параметр. **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**. Значение по умолчанию — –1, которое указывает, что все символы или ветви копируется из текущей позиции в [EOS.](eos-property-ado.md)|

## <a name="remarks"></a>Заметки

Этот метод копирует указанное количество символов или ветвей, начиная с текущей позиции, указанной [свойством Position.](position-property-ado.md) Если указанное число превышает доступное количество в до **EOS,** копируется только символы или количество ветвей из текущей позиции в **EOS.** Если *NumChars* имеет значение –1 или пропущено, копируется все символы или количество символов или ветвей, начиная с текущей позиции.

Если в потоке назначения есть символы или ветви, все содержимое за пределами точки, в которой заканчивается копия, остается без усеченного. **Положение** становится вехой сразу после последнего скопированного byte. Если вы хотите усечение этих данных, вызовите [SetEOS.](seteos-method-ado.md)

**CopyTo** следует использовать для копирования  данных в поток назначения того же типа, что и исходный **Поток** (их параметры свойства **Type** — **adTypeText** или **adTypeBinary).** Для **текстовых объектов Stream** можно изменить параметр свойства [Charset](charset-property-ado.md) конечного **потока** для перевода из одного набора символов в другой. Кроме того, текстовые **объекты Stream** можно успешно скопировать в двоичные объекты **Stream,** но двоичные объекты **Stream** нельзя скопировать в текстовые **объекты Stream.**

