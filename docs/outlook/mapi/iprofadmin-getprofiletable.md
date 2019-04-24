---
title: Ипрофадминжетпрофилетабле
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309550"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице профилей — таблице, содержащей сведения обо всех доступных профилях.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Всегда имеет значение NULL.
    
 _Лпптабле_
  
> вышли Указатель на указатель на таблицу профилей.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица профилей успешно получена.
    
## <a name="remarks"></a>Замечания

Метод **ипрофадмин:: жетпрофилетабле** предоставляет доступ к таблице профилей, которая содержит одну строку для каждого доступного профиля. В каждой строке имеется только два столбца: отображаемое имя профиля и флаг, указывающий, является ли профиль установленным по умолчанию. 
  
Профили, которые были удалены или используются, но помечены для удаления, не включаются в таблицу профилей. Таблица профилей является статической; последующие добавления и удаления профилей не отражаются в таблице. 
  
Если профили не существуют, **жетпрофилетабле** возвращает таблицу с нулевыми строками. 
  
Дополнительные сведения о таблице Profile содержатся в статье [Profile Tables](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маиндлг. cpp  <br/> |Кмаиндлг:: Оншовпрофилес  <br/> |MFCMAPI использует метод **ипрофадмин:: жетпрофилетабле** , чтобы получить таблицу профилей, отображаемую в новом диалоговом окне.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

