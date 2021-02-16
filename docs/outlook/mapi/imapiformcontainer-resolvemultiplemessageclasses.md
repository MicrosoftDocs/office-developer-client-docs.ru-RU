---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412543"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Разрешит группу классов сообщений в их формы в контейнере формы и возвращает массив информационных объектов формы для этих форм.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Параметры

 _pMsgClassArray_
  
> [in] Указатель на массив, содержащий имена классов сообщений, которые необходимо разрешить. Имена классов сообщений всегда являются строками ANSI, а не Юникодом.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет решением классов сообщений. Можно установить следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Должны быть разрешены только строки класса сообщений, точно совпадают.
    
 _ppfrminfoarray_
  
> [out] Указатель на указатель на массив информационных объектов формы. Если клиентские приложения проходят NULL в  _параметре pMsgClassArray,_ параметр  _ppfrminfoarray_ содержит объекты сведений формы для всех форм в контейнере. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Клиентские приложения вызывать метод **IMAPIFormContainer::ResolveMultipleMessageClasses,** чтобы разрешить группу классов сообщений в формы в контейнере формы. Массив информационных объектов формы, возвращаемого в  _параметре ppfrminfoarray,_ обеспечивает дополнительный доступ к каждому свойству формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы разрешить группу классов сообщений в формы, передав массив имен классов сообщений для разрешения. Чтобы разрешение было точным (то есть, чтобы предотвратить разрешение базового класса класса сообщения), флаг MAPIFORM_EXACTMATCH можно передать в _параметре ulFlags._ 
  
Если класс сообщения не может быть разрешен в форму, для этого класса сообщения возвращается NULL в массиве сведений формы. Поэтому даже если метод возвращает S_OK, не следует предполагать, что все классы сообщений успешно разрешены. Вместо этого проверьте значения в возвращаемом массиве.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI использует метод **IMAPIFormContainer::ResolveMultipleMessageClasses** для поиска формы, связанной с набором классов сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

