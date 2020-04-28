---
title: Объект Stream (ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1f6d7e8f64f6b14ea699006fc0461cdf0ded2a06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308486"
---
# <a name="stream-object-ado"></a>Объект Stream (ADO)


**Область применения**: Access 2013, Office 2013

Представляет поток двоичных данных или текста.

## <a name="remarks"></a>Примечания

В иерархических иерархиях, таких как файловая система или система электронной почты, [записи](record-object-ado.md) могут иметь двоичный поток по умолчанию, связанный с файлом, который содержит содержимое файла или сообщения электронной почты. Объект **Stream** можно использовать для управления полями или записями, содержащими эти потоки данных. Объект **Stream** можно получить следующими способами:

  - С URL-адреса, указывающего на объект (обычно это файл), содержащий двоичные данные или текстовые данные. Этот объект может быть простым документом, объектом **Record** , представляющим структурированный документ, или папкой.

  - , Открыв объект **Stream** по умолчанию, связанный с объектом **Record** . Вы можете получить поток по умолчанию, связанный с объектом **Record** при открытии **записи** , чтобы исключить круговой путь только для открытия потока.

  - Путем создания экземпляра объекта **Stream** . Эти объекты **Stream** можно использовать для хранения данных в целях приложения. В отличие от **потока** , связанного с URL-адресом, или **потока** **записи**по умолчанию, у экземпляра **потока** по умолчанию нет связи с базовым источником.

С помощью методов и свойств объекта **Stream** можно выполнить следующие действия:

  - Откройте объект **Stream** из **записи** или URL-адреса с помощью метода [Open](open-method-ado-stream.md) .

  - Закройте **поток** с помощью метода [Close](close-method-ado.md) .

  - Входные байты или текст в **поток** с помощью методов [Write](write-method-ado.md) и [WriteText](writetext-method-ado.md) .

  - Считывание байтов из **потока** с помощью методов [Read](read-method-ado.md) и [ReadText](readtext-method-ado.md) .

  - Запишите все данные **потока** в БУФЕРе ADO в базовый объект с помощью метода [flush](flush-method-ado.md) .

  - Скопируйте содержимое **потока** в другой **поток** с помощью метода [CopyTo](copyto-method-ado.md) .

  - Управление тем, как линии считываются из исходного файла с помощью метода [SkipLine](skipline-method-ado.md) и свойства [LineSeparator](lineseparator-property-ado.md) .

  - Определите положение конца потока с помощью свойства [EOS](eos-property-ado.md) и метода [SetEOS](seteos-method-ado.md) .

  - Сохранение и восстановление данных в файлах с помощью методов [SaveToFile](savetofile-method-ado.md) и [LoadFromFile](loadfromfile-method-ado.md) .

  - Укажите кодировку, используемую для хранения **потока** со свойством [CharSet](charset-property-ado.md) .

  - Остановка асинхронной операции **потока** с помощью метода [Cancel](cancel-method-ado.md) .

  - Определите количество байтов в **потоке** с помощью свойства [size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) .

  - Управление текущей позицией в **потоке** с помощью свойства [position](position-property-ado.md) .

  - Определите тип данных в **потоке** с помощью свойства [Type](type-property-ado-stream.md) .

  - Определение текущего состояния **потока** (закрытое, открытое или выполняемое) со свойством [State](state-property-ado.md) .

  - Укажите режим доступа для **потока** с помощью свойства [mode](mode-property-ado.md) .

> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически будут вызывать [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [абсолютные и относительные URL-адреса](absolute-and-relative-urls.md).


