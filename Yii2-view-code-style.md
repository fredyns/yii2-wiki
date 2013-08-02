The following code style is used for Yii 2.x core and official extensions view files. We aren't forcing you to use this code style for your application. Feel free to choose what suits you better.

```php
<?php
// Leading PHP tag is a must in every template file. Empty line after leading PHP tag is also required.

// Describe input variables passed by controller here.
/**
 * @var yii\base\View $this
 * @var yii\widgets\ActiveForm $form
 * @var app\models\Post[] $posts
 * @var app\models\ContactMessage $contactMessage
 */
// Empty line below is necessary.

// Namespaced classes declaration.
use yii\helpers\Html;
use yii\widgets\ActiveForm;
// Empty line below is necessary.

// Set context properties, call its setters, do other things.
$this->title = 'Posts';
?>
<!-- Separate PHP blocks are preferred for foreach, for, if etc. -->
<?php foreach($posts as $post): ?>
	<!-- Note indentation level here. -->
	<h2><?php echo Html::encode($post['title']); ?></h2>
	<p><?php echo Html::encode($post['shortDescription']); ?></p>
<!-- `endforeach;`, `endfor;`, `endif;`, etc. should be used instead of `}` in case multiple PHP blocks are used -->
<?php endforeach; ?>

<!-- Widget declaration may or may not be exploded into multiple LOCs. -->
<?php $form = ActiveForm::begin(array(
	'options' => array('id' => 'contact-message-form'),
	'fieldConfig' => array('inputOptions' => array('class' => 'common-input')),
)); ?>
	<!-- Note indentation level here. -->
	<?php echo $form->field($contactMessage, 'name')->textInput(); ?>
	<?php echo $form->field($contactMessage, 'email')->textInput(); ?>
	<?php echo $form->field($contactMessage, 'subject')->textInput(); ?>
	<?php echo $form->field($contactMessage, 'body')->textArea(array('rows' => 6)); ?>

	<div class="form-actions">
		<?php echo Html::submitButton('Submit', array('class' => 'common-button')); ?>
	</div>
<!-- Ending widget call should have individual PHP tag. -->
<?php ActiveForm::end(); ?>
<!-- Trailing newline character is mandatory. -->

```