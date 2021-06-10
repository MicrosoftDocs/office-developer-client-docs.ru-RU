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

В иерархиях, структурированных на дереве, таких как [](record-object-ado.md) файловая система или система электронной почты, запись может иметь двоичный поток битов, связанных с ним по умолчанию, который содержит содержимое файла или электронной почты. Объект **Stream** можно использовать для управления полями или записями, содержащими эти потоки данных. Объект **Stream** можно получить таким образом:

  - От URL-адреса, указыващего на объект (как правило, файл), содержащий двоичные или текстовые данные. Этот объект может быть простым документом, **объектом Record,** представляющим структурированный документ, или папкой.

  - Открыв объект Stream **по** умолчанию, связанный с **объектом Record.** Вы можете получить поток по умолчанию, связанный с объектом **Запись,** когда запись открыта, чтобы исключить круговую поездку только для открытия потока. 

  - Моментирование объекта **Stream.** Эти **объекты Stream** можно использовать для хранения данных для целей приложения. В отличие от **потока,** связанного  с URL-адресом или  потоком записи по **умолчанию,** мгновенный поток по умолчанию не имеет связи с исходным источником по умолчанию.

С помощью методов и свойств объекта **Stream** можно сделать следующее:

  - Откройте объект **Stream** из **записи** или URL-адреса методом [Open.](open-method-ado-stream.md)

  - Закрой **поток** [методом Close.](close-method-ado.md)

  - Ввод bytes или text to a **Stream** с помощью методов [Write](write-method-ado.md) и [WriteText.](writetext-method-ado.md)

  - Чтение bytes из **потока** с помощью методов [Чтение](read-method-ado.md) и [ReadText.](readtext-method-ado.md)

  - **Записывайте все данные Потока** в буфере ADO на объект с помощью метода [Flush.](flush-method-ado.md)

  - Скопируйте содержимое потока в  другой **поток** с помощью метода [CopyTo.](copyto-method-ado.md)

  - Управление чтением строк из исходных файлов с помощью метода [SkipLine](skipline-method-ado.md) и [свойства LineSeparator.](lineseparator-property-ado.md)

  - Определите конец положения потока с помощью [свойства EOS](eos-property-ado.md) и [метода SetEOS.](seteos-method-ado.md)

  - Сохранение и восстановление данных в файлах с помощью [методов SaveToFile](savetofile-method-ado.md) и [LoadFromFile.](loadfromfile-method-ado.md)

  - Укажите набор символов, используемый для хранения **потока** с [свойством Charset.](charset-property-ado.md)

  - Остановите операцию асинхронного **потока** с помощью метода [Отмена.](cancel-method-ado.md)

  - Определите количество bytes в **потоке** с [свойством Size.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream)

  - Управление текущей позицией в **потоке** с помощью [свойства Position.](position-property-ado.md)

  - Определите тип данных в **потоке** с [свойством Type.](type-property-ado-stream.md)

  - Определите текущее состояние **потока** (закрытого, открытого или исполняемого) с [государственным свойством.](state-property-ado.md)

  - Укажите режим доступа для **потока с** [свойством Mode.](mode-property-ado.md)

> [!NOTE]
> URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)


