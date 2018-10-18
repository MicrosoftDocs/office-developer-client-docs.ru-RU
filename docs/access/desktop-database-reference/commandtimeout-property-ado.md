---
<<<<<<< Название HEAD: TOCTitle свойство CommandTimeout (ADO): свойство CommandTimeout (ADO) === название: свойство CommandTimeout (ADO) TOCTitle: свойство CommandTimeout (ADO)
>>>>>>> главные ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15) ms:contentKeyID: 48546714 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231124 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="commandtimeout-property-ado"></a>CommandTimeout Property (ADO)
=======
# <a name="commandtimeout-property-ado"></a>Свойство CommandTimeout (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает время ожидания при выполнении команды перед завершается и генерируется ошибка.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает значение типа **Long** , указывающее, в секундах, как долго следует ожидать выполнения команды. Значение по умолчанию — 30.

## <a name="remarks"></a>Замечания

<<<<<<< HEAD используйте свойство **CommandTimeout** объекта [подключения](connection-object-ado.md) или [команды](command-object-ado.md) , чтобы разрешить отмены для вызова метода [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) , из-за задержки от. Используйте сетевой трафик или высокая интенсивность операций сервера. Если в свойстве **CommandTimeout** этого времени до завершения выполнения команды, возникает ошибка, и ADO отменяет команду. Если задать свойству присваивается значение 0, ADO ожидает неопределенное время до завершения выполнения. Убедитесь, что источник поставщика и данных, к которому написании кода поддержки **CommandTimeout** функциональные возможности.
=== Свойство **CommandTimeout** объекта [подключения](connection-object-ado.md) или [команду](command-object-ado.md) чтобы разрешить отмены для вызова метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) , из-за задержки от. Используйте сетевой трафик или высокая интенсивность операций сервера. Если в свойстве **CommandTimeout** этого времени до завершения выполнения команды, возникает ошибка, и ADO отменяет команду. Если задать свойству присваивается значение 0, ADO ожидает неопределенное время до завершения выполнения. Убедитесь, что источник поставщика и данных, к которому написании кода поддержки **CommandTimeout** функциональные возможности.
>>>>>>> master

Параметр **CommandTimeout** на объект **подключения** не оказывает влияния на параметр **CommandTimeout** объекта **команды** на том же **подключения**; то есть свойство **CommandTimeout** объект **команды** не наследует значение **CommandTimeout** объект **подключения** .

На объект **подключения** свойство **CommandTimeout** остается чтения/записи после открытия **подключения** .

