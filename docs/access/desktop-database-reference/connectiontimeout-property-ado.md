---
<<<<<<< Название HEAD: TOCTitle свойство ConnectionTimeout (ADO): свойство ConnectionTimeout (ADO) === название: свойство ConnectionTimeout (ADO) TOCTitle: свойство ConnectionTimeout (ADO)
>>>>>>> главные ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15) ms:contentKeyID: 48548589 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="connectiontimeout-property-ado"></a>ConnectionTimeout Property (ADO)
=======
# <a name="connectiontimeout-property-ado"></a>Свойство ConnectionTimeout (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает время ожидания при установке соединения перед завершается и генерируется ошибка.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает значение типа **Long** , которое указывает, в секундах, время ожидания для подключения открыть. Значение по умолчанию — 15.

## <a name="remarks"></a>Замечания

Используйте свойство **ConnectionTimeout** на объект [подключения](connection-object-ado.md) Если использовать задержки сетевого трафика или высокая интенсивность операций сервера необходимо отменить попытку подключения. Если перед открытием подключения истечения времени от настройки свойства **ConnectionTimeout** , возникает ошибка, и ADO отменяет попытку. Если задать свойству присваивается значение 0, ADO будет ждать неограниченное время открытия подключения. Убедитесь, что поставщик, к которому написании кода поддерживает функциональную возможность **ConnectionTimeout** .

Свойство **ConnectionTimeout** — чтение и запись в случае подключения закрытой и только для чтения при открытии.

