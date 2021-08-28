## Syntax

<table class="syntab">
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2">jackknife_options</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd section">
<td colspan="3">SE</td>
</tr>
<tr class="even">
<td class="normal"></td>
<td><code class="command" data-options="mse">mse</code></td>
<td>use MSE formula for variance</td>
</tr>
<tr class="odd">
<td class="normal"></td>
<td><code class="command" data-options="nodots">nodots</code></td>
<td>suppress replication dots</td>
</tr>
<tr class="even">
<td class="normal"></td>
<td><code class="command" data-options="dots(#)">dots(#)</code></td>
<td>display dots every <var class="command">#</var> replications</td>
</tr>
<tr class="odd">
<td class="normal"></td>
<td>[<strong></strong>](http://www.stata.com/help.cgi?prefix_saving_option)
<ul>
</ul>
ving(<var class="command">filename</var><strong>, ...)</strong></td>
<td>save results to <var class="command">filename</var></td>
</tr>
<tr class="even">
<td class="normal"></td>
<td><code class="command" data-options="keep">keep</code></td>
<td>keep pseudovalues</td>
</tr>
<tr class="odd">
<td class="normal"></td>
<td><code class="command" data-options="v">verbose</code></td>
<td>display the full table legend</td>
</tr>
<tr class="even">
<td class="normal"></td>
<td><code class="command" data-options="noi">noisily</code></td>
<td>display any output from <var class="command">command</var></td>
</tr>
<tr class="odd">
<td class="normal"></td>
<td><code class="command" data-options="tr">trace</code></td>
<td>trace <var class="command">command</var></td>
</tr>
<tr class="even">
<td class="normal"></td>
<td><code class="command" data-options="ti">title(text)</code></td>
<td>use <var class="command">text</var> as the title for results</td>
</tr>
<tr class="odd">
<td class="normal"></td>
<td><code class="command" data-options="nodrop">nodrop</code></td>
<td>do not drop observations</td>
</tr>
<tr class="even">
<td class="normal"></td>
<td><code class="command" data-options="reject(exp)">reject(exp)</code></td>
<td>identify invalid results</td>
</tr>
</tbody><tfoot>
<tr class="odd footnote">
<td colspan="3"><code class="command">saving()</code>, <code class="command">keep</code>, <code class="command">verbose</code>, <code class="command">noisily</code>, <code class="command">trace</code>, <code class="command">title()</code>, <code class="command">nodrop</code>, and <code class="command">reject()</code> are not shown in the dialog boxes for estimation commands. <span data-options="description">{marker description}_<span>{nobreak None}_ <span>{title None:Description}_ <span>{pstd None}_ <code class="command">svy</code> accepts more options when performing jackknife variance estimation. <span data-options="options">{marker options}_<span>{nobreak None}_ <span>{title None:Options}_ <span>{dlgtab None:SE}_ <span>{phang None}_ <code class="command" data-options="mse">mse</code> specifies that <code class="command">svy</code> compute the variance by using deviations of the replicates from the observed value of the statistics based on the entire dataset. By default, <code class="command">svy</code> computes the variance by using deviations of the pseudovalues from their mean. <span>{phang None}_ <code class="command" data-options="nodots">nodots</code> suppresses display of the replication dots. By default, one dot character is printed for each successful replication. A red `x' is displayed if <var class="command">command</var> returns with an error, `e' is displayed if at least one of the values in the <var class="command">exp_list</var> is missing, `n' is displayed if the sample size is not correct, and a yellow `s' is displayed if the dropped sampling unit is outside the subpopulation sample. <span>{phang None}_ <code class="command" data-options="dots(#)">dots(#)</code> displays dots every <var class="command">#</var> replications. <code class="command">dots(0)</code> is a synonym for <code class="command">nodots</code>. <span>{phang None}_ <code class="command" data-options="saving()">saving()</code>, <code class="command" data-options="keep">keep</code>, <code class="command" data-options="verbose">verbose</code>, <code class="command" data-options="noisily">noisily</code>, <code class="command" data-options="trace">trace</code>, <code class="command" data-options="title()">title()</code>, <code class="command" data-options="nodrop">nodrop</code>, <code class="command" data-options="reject()">reject()</code>; see [<strong>[SVY]</strong> svy jackknife](http://www.stata.com/help.cgi?svy_jackknife).</td>
</tr>
</tfoot>

</table>