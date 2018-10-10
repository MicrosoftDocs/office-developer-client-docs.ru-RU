---
title: ActiveConnection Property (ADO MD)
TOCTitle: ActiveConnection Property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0743771ee9cee096f8de3d91d793ea8cf81af2ea
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482347"
---
# <a name="activeconnection-property-ado-md"></a>ActiveConnection Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Указывает, какие объект ADO- [подключение](connection-object-ado.md) текущий набор ячеек и каталогов в настоящее время принадлежит.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Variant** , содержащее строку, определяющую подключения или объект **подключения** . Значение по умолчанию будет пустым.

## <a name="remarks"></a>Замечания

Это свойство можно задать допустимый объект ADO- **подключение** или это допустимая строка подключения. Если это свойство строки подключения, поставщик создает новый объект **подключения** с помощью этого определения и открывает подключение.

Если вы используете **ActiveConnection** аргумента метода [Open](open-method-ado-md.md) открыть объект [ячеек](cellset-object-ado-md.md) , свойство **ActiveConnection** наследуют значение аргумента.

Установка **ActiveConnection** свойства объекта [каталога](catalog-object-ado-md.md) значение **Nothing** освобождает связанных данных, включая данные в коллекции [CubeDefs](cubedefs-collection-ado-md.md) и любые связанных [измерений](dimension-object-ado-md.md), [иерархий](hierarchy-object-ado-md.md)и [уровень](level-object-ado-md.md) и объекты [члена](member-object-ado-md.md) . Закрытие объект **подключения** , которая использовалась при открытии **каталога** действует как свойства **ActiveConnection** значение **Nothing**.

Изменение базы данных по умолчанию подключения ссылается свойство **ActiveConnection** объекта **каталога** нарушает содержимого **каталога**.

При попытке изменить свойство **ActiveConnection** open объекта **ячеек** , произойдет ошибка.


> [!NOTE]
> <P>В Visual Basic не забудьте ключевого слова <STRONG>Set</STRONG> при задании свойства <STRONG>ActiveConnection</STRONG> для объекта <STRONG>подключения</STRONG> . Если опустить ключевого слова <STRONG>Set</STRONG> , вам будет фактически свойства <STRONG>ActiveConnection</STRONG> равно объект <STRONG>подключения</STRONG> по умолчанию свойства <STRONG>ConnectionString</STRONG>. Код будет работать; Тем не менее будет создать дополнительные подключения к источнику данных, который может иметь негативное влияние.</P>



При использовании поставщика данных MSOLAP, задайте источника данных в строке подключения с именем сервера и присвоено имя каталога базу данных из источника данных. Для подключения к файлу куба, отключены от сервера, задайте расположение полный путь. Файл КУБ. В любом случае значение имени поставщика и имени поставщика. Например следующую строку подключается к каталогу с именем Bobs видео хранилища на сервере с именем имя сервера с поставщиком MSOLAP:

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

Следующая строка подключается к файлу локального куба в расположении C:\\MSDASDK\\примеры\\oledb\\olap\\данные\\bobsvid.cub:

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

