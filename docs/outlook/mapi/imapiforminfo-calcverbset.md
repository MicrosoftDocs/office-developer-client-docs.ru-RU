---
title: Имапиформинфокалквербсет
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321700"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на полный набор команд, которые использует форма.
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющих тип возвращаемых строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Возвращаемые строки представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.
    
 _Ппмапивербаррай_
  
> вышли Указатель на указатель на возвращаемую структуру [смапивербаррай](smapiverbarray.md) , содержащую команды формы. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
МАПИ_Е_БАД_ЧАРВИДС 
  
> Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Замечания

Клиентские приложения вызывают метод **имапиформинфо:: калквербсет** для получения указателя на набор глаголов, используемых формой. В структуре **смапивербаррай** , возвращаемой в параметре _ппмапивербаррай_ , команды возвращаются в порядке числа индексов; Индекс каждой команды находится в его члене **лверб** . Клиентские приложения могут использовать массив команд для динамической сборки меню, скрытия или отображения кнопок и т. д. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мфкаутпут. cpp  <br/> |_Аутпутформинфо  <br/> |MFCMAPI использует метод **имапиформинфо:: калквербсет** при записи выходных данных отладки для объектов данных формы.  <br/> |
   
## <a name="see-also"></a>См. также



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

