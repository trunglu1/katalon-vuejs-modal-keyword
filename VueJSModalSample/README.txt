This project is a sample test case of using VueJS Modal Plugin. Please follow these steps below to using this plugin: 

1. Create/Open Katalon project.
2. Select Project > Settings > External Libraries
3. Add VueJSModalKeywords.jar enclosed then click OK
4. On test case file, import com.kms.katalon.webui.keyword.vuejs.ModalKeywords then use this plugin as below example.
5. Hover on import com.kms.katalon.webui.keyword.vuejs.ModalKeywords, right click, then select Open Declaration
6. Select Attach Source on Class File Editor page, add VueJSModalKeywords_sources.jar to External location to attach javadoc.

----------------------------
import com.kms.katalon.webui.keyword.vuejs.ModalKeywords

WebUI.openBrowser('https://vuejs.org/v2/examples/modal.html')

TestObject to = findTestObject('vuejs/modal/divDefaultModalContainer')

assert ModalKeywords.getModalTitleText(to).contains('custom header')

assert ModalKeywords.getModalContentText(to).contains('default body')

ModalKeywords.clickConfirmButtonByText(to, 'OK')
----------------------------