---
title: Метод stat - ActiveX Data Objects (ADO)
TOCTitle: Stat Method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc4ff8076ec07d065ba932ef0e0017edb97e703
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606957"
---
# <a name="stat-method-ado"></a>Stat Method (ADO)


**Применимо к**: Access 2013 | Office 2013

Извлекает сведения о объект **Stream** .

## <a name="syntax"></a>Синтаксис

Длинные *потока*. Статистика (*StatStg*, *StatFlag*)

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Значение типа long, указывающее состояние операции.

## <a name="parameters"></a>Параметры

  - *StatStg*

  - Структура STATSTG, будут заполнены сведения о потоке. Реализация метода Stat объект ADO Stream не заполните все поля структуры.

  - *StatFlag*

  - Указывает, что этот метод не возвращает некоторые элементы в структуре STATSTG сэкономить операция выделения памяти. Значения берутся из перечисления STATFLAG.  
      
    Перечисление STATFLAG имеет два значения
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Константа</p></th>
    <th><p>Значение</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>STATFLAG_DEFAULT</p></td>
    <td><p>0</p></td>
    </tr>
    <tr class="even">
    <td><p>STATFLAG_NONAME</p></td>
    <td><p>1</p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a>Замечания

В следующих полях структуры STATSTG заполняет версии Stat метода, реализованного в объекте ADO Stream:

  - *pwcsName*

  - Строка, содержащая имя потока, если он доступен и StatFlag значение STATFLAG\_NONAME не указан.

  - *cbSize*

  - Указывает размер массива байтов или потока в байтах.

  - *mtime*

  - Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.

  - *CTime*

  - Указывает время создания для данного объекта хранилища, потока или массива байтов.

  - *atime*

  - Указывает время последнего обращения к этой хранилища, потока или массива байтов.

Если STATFLAG\_NONAME указан в параметре StatFlag, имя потока не возвращается.

Если STATFLAG\_NONAME не указан в параметре StatFlag и нет имя не для текущего потока, это значение будет E\_NOTIMPL.

