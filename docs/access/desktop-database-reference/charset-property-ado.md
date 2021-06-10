---
title: Свойство Charset (ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca4640940c217fd81cac4ba1d8ffaf769b506fe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296390"
---
# <a name="charset-property-ado"></a>Свойство Charset (ADO)


**Область применения**: Access 2013, Office 2013

Указывает набор символов, в который необходимо [](stream-object-ado.md) перевести содержимое текстового потока для хранения в внутреннем буфере объектов Stream.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает **значение String,** которое указывает набор символов,  в который будет переведено содержимое потока. Значение по умолчанию — "Unicode". Допустимые значения — это типичные строки, переданные интерфейсу в качестве строк набора символов Интернета (например, "iso-8859-1", "Windows-1252" и т.д.). Список строк набора символов, известных системе, см. в подкайке базы данных HKEY \_ CLASSES \_ ROOT \\ MIME \\ в Windows \\ Реестре.

## <a name="remarks"></a>Примечания

В объекте **text Stream** текстовые данные хранятся в наборе символов, заданном **свойством Charset.** По умолчанию — Юникод. Свойство **Charset** используется для преобразования данных, вступающих в **поток** или вылетеющих из **потока.** Например, если  поток содержит данные ISO-8859-1 и эти данные копируются в BSTR, объект **Stream** преобразует данные в Unicode. Обратное также верно.

Для открытого **потока** текущая [позиция](position-property-ado.md) должна быть в начале потока (0), чтобы иметь возможность установить **Charset**. 

**Charset** используется только с текстовыми **объектами Stream** [(Type](type-property-ado-stream.md) **is adTypeText).** Это свойство игнорируется, **если Type** **является adTypeBinary.**

